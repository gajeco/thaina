# Landing page — Dra. Thainá Lima

Site estático, um único arquivo: `index.html`. Sem build, sem dependências.
Abra pelo servidor HTTP (necessário para o manifesto PWA resolver corretamente):

```bash
python -m http.server 8000
```

## Publicar fotos na seção "Casos"

Cada um dos 6 cards já tem uma área de imagem reservada em
`<div class="gcard__media">`, com a tag `<img>` comentada logo dentro.

1. Coloque o arquivo em `assets/caso-<slot>.jpg`, proporção 4:5 (ex.: 900×1125).
2. No `index.html`, descomente o `<img>` dentro do `.gcard__media` do card desejado.
3. Troque o `alt="..."` por uma descrição real da imagem.

Slots: `perfil`, `labial`, `terco-medio`, `frontal`, `mandibula`, `panorama`.

**O layout não muda** — nem o grid, nem a ordem, nem a altura dos cards vizinhos.
Isso porque `.gcard__media` tem `aspect-ratio:4/5` sempre, vazia ou não, e o
`img` usa `object-fit:cover`. A altura já está prevista antes da foto existir,
então inseri-la não empurra o texto nem desalinha a linha de cards.

## Regra ética

Só publique foto de paciente com **autorização por escrito**. Sem edição de cor
ou forma, sem comparação de antes e depois. O `onerror="this.remove()"` faz a
imagem sumir se o arquivo não for encontrado, deixando o placeholder visível.

## Estrutura

```
index.html            página inteira (HTML + CSS + JS inline)
COPY-DECK.md          copy, decisões de design e checklist editorial
assets/
  favicon.svg, favicon-32.png, apple-touch-icon.png
  icon-192.png, icon-512.png, icon-maskable-512.png
  site.webmanifest
  dra-thaina-hero.jpg, dra-thaina-consulta.jpg, dra-thaina-formacao.jpg
img/                  fotos originais preservadas (fonte dos exports acima)
```

## Antes de publicar

- [ ] Conferir o favicon em 16px, aba escura e home screen do Android
- [ ] Conferir `apple-mobile-web-app-status-bar-style="black-translucent"` em iPhone com notch
- [ ] Consentimento por escrito de cada paciente antes de descomentar qualquer `<img>`
- [ ] Validar com a profissional as faixas de duração e as alegações de segurança
- [ ] Testar os 22 links `wa.me` com `?text=` em Android e iOS
- [ ] Confirmar que `wa.me/557583527689` abre a conversa com o texto colado
- [ ] Substituir o domínio provisório `drathainalima.com.br` pelo definitivo