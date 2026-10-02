# Landing page — Dra. Thainá Lima

Site estático, um único arquivo: `index.html`. Sem build, sem dependências.
Abra pelo servidor HTTP (necessário para o manifesto PWA resolver corretamente):

```bash
python -m http.server 8000
```

## Casos: 6 cards com foto reservada

A seção `#galeria` tem os **6 cards**, cada um com a moldura da foto já reservada
em `.gcard__media` (`aspect-ratio:4/5`, moldura tracejada). O bloco está **vazio**
de propósito: a altura do card existe antes de a foto existir.

Para publicar a foto de um caso:

1. Coloque o arquivo em `assets/` com o nome do `data-slot` do card:
   `perfil`, `labial`, `terco-medio`, `frontal`, `mandibula`, `panorama`.
   Proporção 4:5 (ex.: 900×1125).
2. Cole o `<picture>` dentro do `.gcard__media` correspondente:

```html
<div class="gcard__media" data-slot="perfil">
  <picture>
    <source type="image/webp" srcset="assets/caso-perfil.webp">
    <img src="assets/caso-perfil.jpg" alt="Descrição real da imagem"
         width="900" height="1125" loading="lazy" decoding="async">
  </picture>
</div>
```

Nada mais muda: nem o CSS, nem o grid, nem a ordem, nem a altura dos vizinhos.
`.gcard__media picture` e `.gcard__media img` já estão dimensionados
(`width/height:100%` + `object-fit:cover`), então a foto cobre a moldura e
preenche o quadro. Um `<img>` sozinho também funciona, sem `<picture>`.

Não precisa remover nada, não precisa de `onerror` e não há `<img>` comentado
esperando no HTML. Verificado por medição: inserir a imagem nos 6 cards mantém
altura da seção, altura da página e posição de todos os títulos idênticas
(CLS 0) em 320px e 1440px.

Slots: `perfil`, `labial`, `terco-medio`, `frontal`, `mandibula`, `panorama`.

## Regra ética

Só publique foto de paciente com **autorização por escrito**. Sem edição de cor
ou forma, sem comparação de antes e depois.

A seção Casos **não tem** mais a nota ética visível: ela foi removida a pedido.
A regra continua valendo — só publique imagem com autorização por escrito e
observe o aviso legal do rodapé, que é o texto regulatório que permanece na página.

## Estrutura

```
index.html            página inteira (HTML + CSS + JS inline)
COPY-DECK.md          copy, decisões de design e checklist editorial
assets/               todas as imagens usadas pela página
  favicon.svg, favicon-32.png, apple-touch-icon.png
  icon-192.png, icon-512.png, icon-maskable-512.png
  site.webmanifest
  dra-thaina-hero.jpg, dra-thaina-consulta.jpg, dra-thaina-formacao.jpg
  dra-thaina-hero.webp, dra-thaina-hero-800.webp
  dra-thaina-consulta.webp, dra-thaina-consulta-750.webp
  dra-thaina-formacao.webp, dra-thaina-formacao-600.webp
  og-preview.jpg
```

A página usa exclusivamente `assets/`. Não há outra pasta de imagens no projeto.

## Imagens

As três fotos principais usam `<picture>` com WebP responsivo e fallback JPEG:

| Papel     | WebP                            | JPEG fallback            | `sizes`                        |
| --------- | ------------------------------- | ------------------------ | ------------------------------ |
| Hero      | `-800.webp` / full `1200×1500`  | `dra-thaina-hero.jpg`    | `(min-width:980px) 46vw, 100vw` |
| Consulta  | `-750.webp` / full `1125×1500`  | `dra-thaina-consulta.jpg`| `42vw`                         |
| Formação  | `-600.webp` / full `900×1125`   | `dra-thaina-formacao.jpg`| `34vw`                         |

Regra ao editar:

- nunca trocar `srcset`/`sizes` sem atualizar o `<link rel="preload">` do hero
  no `<head>` — preload divergente causa download duplicado;
- manter `width`/`height` e o `aspect-ratio` do `.ph`, senão o CLS volta;
- todo `<img>` precisa de `width`, `height`, `loading`, `decoding` e `alt`
  real (o `alt` descreve a imagem, não o serviço);
- as galerias de consulta e formação já têm altura reservada por CSS, então
  trocar o arquivo não muda o layout.

`og-preview.jpg` (1200×630) é a imagem de compartilhamento usada por
`og:image` e `twitter:image`.

## Auditoria de assets

Todos os 17 arquivos de `assets/` estão em uso: 6 ícones + manifesto, 3 fotos em
`<picture>` (WebP + JPEG), 6 variantes WebP e a imagem de compartilhamento. Não
há arquivo órfão nem referência quebrada. Para reconferir depois de mexer:

```bash
# arquivoreferenciado por index.html ou pelo manifesto?
$src = (Get-Content index.html -Raw) + (Get-Content assets\site.webmanifest -Raw)
Get-ChildItem assets -File | % { "$($_.Name) -> $(([regex]::Matches($src,[regex]::Escape($_.Name))).Count)" }

# referência a arquivo que não existe?
[regex]::Matches($src,'assets/[A-Za-z0-9._-]+') | % Value | Sort -Unique |
  ? { -not (Test-Path $_) }
```

Os JPEG de fallback (499KB no total) só são baixados por navegador sem WebP —
todos os navegadores atuais usam o WebP. Eles ficam por robustez; remover
significa quebrar o fallback do `<picture>`.

## Antes de publicar

- [ ] Conferir o favicon em 16px, aba escura e home screen do Android
- [ ] Conferir `apple-mobile-web-app-status-bar-style="black-translucent"` em iPhone com notch
- [ ] Conferir a prévia de compartilhamento em `assets/og-preview.jpg` (WhatsApp, LinkedIn, Instagram, X)
- [ ] Validar com a profissional as faixas de duração e as alegações de segurança
- [ ] Confirmar o registro exibido no rodapé, em "A profissional" e no JSON-LD (`CRBM-BA`, habilitação em Biomedicina Estética)
- [ ] Confirmar os horários atendidos (hoje: segunda a sábado, 9h–19h) antes de publicar
- [ ] Testar os 22 links `wa.me` com `?text=` em Android e iOS
- [ ] Confirmar que `wa.me/557583527689` abre a conversa com o texto colado
- [ ] Substituir o domínio provisório `drathainalima.com.br` pelo definitivo
      (`canonical`, `og:url`, JSON-LD e links de WhatsApp)
- [ ] Reexecutar a auditoria de contraste e de alvos de toque a cada mudança de cor
- [ ] Autorização por escrito de cada paciente antes de publicar a foto do caso

## Auditoria já executada

Chrome headless via CDP, em 320, 390, 779, 780, 860, 1019, 1024 e 1440px:

- `CLS: 0` e overflow horizontal `0` em todos os tamanhos;
- nenhum alvo interativo abaixo de 44×44px;
- `.wa-float` some no rodapé e reaparece ao subir (`passouFinal` recalculado por frame);
- nenhum erro de console;
- 227–232 textos renderizados por tamanho, **nenhum** abaixo de WCAG AA
  (pior caso medido: 4.79:1 em `.brand__role`);
- 6 cards em Casos e ângulos, 6 molduras 4:5 reservadas em todos os tamanhos;
- inserir `<picture>` nas 6 molduras mantém altura da seção, altura da página e
  posição de todos os títulos **idênticas** — ou seja, publicar as fotos depois
  não exige mexer em layout nem em CSS.