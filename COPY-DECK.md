# Copy & Layout Deck — Dra. Thainá Lima

Versão 3.1 · espelha `index.html` · arquivo único, sem build.

---

## 1. Regras de ouro

| Item | Definição |
|---|---|
| Objetivo único | Conversão para WhatsApp. Não há formulário em toda a página. |
| Linguagem | 2ª pessoa do singular: "você", "seu rosto". Nunca "a paciente" no texto persuasivo — só no texto técnico/legal. Sem "tu"/"te". |
| Verde `#25D366` | **Exclusivo** do botão flutuante (fundo + ícone). Nenhum outro elemento usa essa cor. |
| CTAs | Todo link de conversão leva o símbolo do WhatsApp (`<use href="#i-wa">`), `target="_blank" rel="noopener"` e mensagem pré-preenchida. |
| Promessa | Proporção, naturalidade e segurança. Nunca "resultado garantido", nunca antes/depois. |
| Durações | Sempre "como referência". Nunca como certeza. |
| Acessibilidade | Alvos ≥ 44px, H1 único, foco visível, contraste AA, `prefers-reduced-motion` respeitado. |
| Domínio | `https://drathainalima.com.br/` é provisório — substituir no `<link rel="canonical">`, no JSON-LD e antes de publicar. |

---

## 2. Paleta

| Token | Valor | Uso |
|---|---|---|
| `--ivory` | `#FBF8F4` | Fundo da página |
| `--sand` | `#F3EAE0` | Faixas alternadas, banda de formação, ícones circulares |
| `--shell` | `#FFFFFF` | Cards, superfícies claras |
| `--ink` | `#1A1815` | Texto principal |
| `--ink-2` | `#3A332C` | Texto secundário |
| `--muted` | `#7C7164` | Legendas e placeholders |
| `--graphite` | `#2A2724` | Botões primários |
| `--graphite-2` | `#211E1B` | Gradiente dos botões |
| `--bronze` | `#A8794F` | Bullets, sublinhados, bordas de destaque |
| `--bronze-deep` | `#7E5738` | Eyebrows, ícones outline, itálico do H1 |
| `--bronze-soft` | `rgba(168,121,79,.34)` | Moldura do hero, tracejado do painel |
| `--gold` | `#C6A46C` | Card lead, chips, rodapé |
| `--line` | `rgba(26,24,21,.12)` | Bordas de 1px |
| `--line-soft` | `rgba(26,24,21,.07)` | Bordas internas, grade dos pilares |
| `--wa` | `#25D366` | **Só** o botão flutuante |

Escala de cinzas sempre morna. Nota: **não existem** `--paper`, `--ink-3` nem `--line` como cor sólida — não usar essa nomenclatura.

---

## 3. Mapa da página

| # | id | Seção | Altura (1440px) | Job |
|---|---|---|---|---|
| 0 | `topbar` | Barra fixa | 72px | Marca, navegação, CTA sempre visível |
| 1 | `hero` | Hero | 1158px | Promessa + foto real + seletor de cidade acima da dobra |
| 2 | `filosofia` | A filosofia | 1595px | Anti-“cara de fazer procedimento” + 4 pilares + **banda de formação** + callout |
| 3 | `procedimentos` | Procedimentos | 1577px | 5 cards com CTA individual |
| 4 | `galeria` | Casos e ângulos | 959px | **6 cards** com espaço de imagem reservado (4:5) para cada slot |
| 5 | `sobre` | A profissional | 991px | Foto 3:4 real, formação, credenciais |
| 6 | `como-funciona` | Três passos | 688px | Jornada, ritmo deliberadamente compacto |
| 7 | `duvidas` | Dúvidas frequentes | 826px | 6 `<details>` + saída de escape |
| 8 | `agendar` | CTA final | 839px | Fechamento segmentado por cidade |
| 9 | `.foot` | Rodapé grafite | 492px | Âncoras, sigilo, legal |

Total **9197px** no desktop. Mobile (390px) ≈ 13036px.
Hierarquia: 1 H1, 7 H2, 15 H3, 2 H4.

---

## 4. Copy final

### 4.0 Topbar

- Marca: **Dra. Thainá Lima** / Biomedicina Estética
- Nav: Filosofia · Procedimentos · Casos · A profissional · Dúvidas
- CTA: `Agendar avaliação`

### 4.1 Hero

| Elemento | Texto |
|---|---|
| Eyebrow | Biomedicina Estética · Bahia |
| H1 | **Não transformamos rostos. *Revelamos presença.*** |
| Sub | Sua imagem em harmonia com a sua identidade. Avaliação individualizada, técnica precisa e resultado que continua parecendo com você. |
| CTA primário | `Agendar avaliação personalizada` |
| CTA secundário | `Ver procedimentos` (outline, âncora `#procedimentos`) |
| Seletor | *Onde você prefere ser atendido(a)?* → `Feira de Santana` · `Irará` |
| Hint (repouso) | Escolha uma cidade e todos os botões desta página enviam a preferência certa. |
| Hint (ativo) | Preferência registrada: {cidade}. Todos os botões enviam essa informação. |
| Links diretos | `Informações sobre Feira de Santana` · `Informações sobre Irará` |
| Badge foto | **Avaliação milimétrica** — Cada traço medido antes de qualquer decisão. |
| Faixa (4) | Naturalidade/Antes de mais nada · Individualização/Um plano por pessoa · Segurança/Técnica habilitada · Acolhimento/Você é ouvida |

### 4.2 A filosofia

- H2: **Harmonização é revelar o que já existe em você.**
- Lead 1: O medo mais comum não é a dor: é a **“cara de fazer procedimento”**. Ele nasce de padrões repetidos e promessas impossíveis.
- Lead 2: Aqui, o trabalho começa pelo oposto — entender a sua biometria antes de encostar em qualquer produto.
- Bullets:
  - Nariz, lábios e queixo lidos em conjunto, nunca como peças isoladas.
  - Medidas e proporções estudadas antes de qualquer decisão.
  - Se alguém nota o procedimento antes de notar a beleza, refizemos a conta.
- Pull quote: *O resultado tem que ser lido como presença, nunca como mudança.*

**Pilares (4)**

| # | Título | Texto |
|---|---|---|
| 1 | Avaliação milimétrica | Medidas e assimetrias estudadas antes. Nada estimado no olho, nada copiado de outro caso. |
| 2 | Técnica sem exagero | Conservação dos traços. O rosto fica mais harmonioso, nunca estranho — nem para você, nem para os outros. |
| 3 | Segurança como regra | Produtos certificados e contraindicações avaliadas. Se não é seguro para você, não é feito. |
| 4 | Acolhimento sem pressa | Tempo para escutar e explicar cada alternativa em linguagem simples — com honestidade sobre o que é possível. |

**Banda de formação** (nova — substitui a galeria de fotos institucionais)

Foto `assets/dra-thaina-formacao.jpg` à esquerda em coluna de 320px (4:5), texto à direita, abaixo do `.grid-2` e acima do callout. Fundo `--sand`, borda `--line-soft`, raio `--r-lg`.

- Eyebrow: Formação contínua
- H3: **Cada técnica se atualiza. O método também.**
- Lead: A harmonização facial evolui rápido, e acompanhar esse movimento é parte do trabalho. A participação em mentorias de harmonização *full face* mantém a técnica alinhada ao que é referência na área — sempre com biossegurança como base.
- Chips: `Mentoria em harmonização full face` · `Dia do Biomédico`
- Selo sobre a foto: **Full Face** / Mentoria

No mobile a banda empilha em coluna única e a foto é limitada a 340px, com o selo reposicionado à esquerda.

**Callout — “E se eu ficar com a aparência artificial?”** (agora em largura total, `max-width:900px`)
> É a pergunta que mais fazemos. O medo é legítimo: protocolos de internet que tratam o rosto como peça de fábrica produziram exatamente esse efeito. Aqui, a quantidade de produto é definida pela medida, não pelo protocolo. Você aprova cada etapa e pode interromper quando quiser.
> CTA: `Tirar essa dúvida no WhatsApp`

### 4.3 Procedimentos

- Eyebrow: Procedimentos
- H2: **Cada procedimento, uma decisão sob medida**
- Lead: Nenhum destes é vendido como pacote. Fale direto com a equipe para entender cada um.

| # | Título | Tagline | Descrição | Bullets |
|---|---|---|---|---|
| 01 | Perfiloplastia | O equilíbrio que faltava entre nariz, lábios e queixo. | Avaliamos o perfil como um todo. Quando um traço desequilibra todos os outros, harmonizar o conjunto devolve a proporção natural — sem que ninguém identifique o que mudou. | Correção de desvios e assimetrias de perfil · Ajuste fino de queixo e mentônio quando indicado · Planejamento das proporções antes da execução |
| 02 | Harmonização facial e corporal | Um plano desenhado para um rosto só — o seu. | A harmonização não é um produto: é a soma de decisões. Face e corpo são tratados em conjunto quando se completam. | Avaliação completa com medidas e fotos · Protocolo combinado entre face e corpo · Planejamento por etapas |
| 03 | Preenchimento labial | Contorno respeitado, zero efeito “bico de pato”. | O erro mais comum não é o volume: é o contorno. Preservamos a transição entre lábio e sorriso — a diferença está em quem olha. | Volume com técnica suportada · Preservação da expressão do sorriso · Resultado discreto e revisável |
| 04 | Toxina botulínica | Expressão livre, rosto que continua sendo o seu. | Suaviza o ruído sem apagar a sua cara — mantendo a capacidade de se expressar, sorrir e se surpreender. | Mapeamento muscular antes da aplicação · Doses calculadas por região · Manutenção preventiva com intervalos honestos |
| 05 | Bioestimuladores | A sua própria produção, reativada devagar. | Para quem perdeu firmeza e quer recuperar estrutura sem alterar a identidade. O resultado aparece de forma progressiva e natural. | Estímulo gradual do colágeno · Melhora de textura e firmeza · Protocolo com intervalos definidos |

Cada card fecha com um `link-wa`: `Quero saber sobre {Perfiloplastia | Harmonização | Preenchimento Labial | Botox | Bioestimuladores}`.

O card 01 usa `.card--lead` — largura dobrada na mesma linha dos demais.

### 4.4 Casos e ângulos

Seção com **6 cards** (`.gal__grid` / `.gcard`), um por slot. Descrições reaproveitadas dos cards de Procedimentos, para não haver copy nova circulando sem revisão.

- Eyebrow: Casos e ângulos
- H2: **Naturalidade é o critério, não a exceção**
- Lead: Cada rosto é uma biometria única. Por isso, casos reais só entram aqui com autorização expressa da paciente — sem edição de cor ou forma e sem comparação de antes e depois.

| # | Título | Tagline | Descrição | Slot de imagem |
|---|---|---|---|---|
| 01 | Perfiloplastia | O equilíbrio que faltava entre nariz, lábios e queixo. | Avaliamos o perfil como um todo. Quando um traço desequilibra todos os outros, harmonizar o conjunto devolve a proporção natural — sem que ninguém identifique o que mudou. | `caso-perfil.jpg` |
| 02 | Preenchimento labial | Contorno respeitado, zero efeito “bico de pato”. | O erro mais comum não é o volume: é o contorno. Preservamos a transição entre lábio e sorriso — a diferença está em quem olha. | `caso-labial.jpg` |
| 03 | Toxina botulínica | Expressão livre, rosto que continua sendo o seu. | Suaviza o ruído sem apagar a sua cara — mantendo a capacidade de se expressar, sorrir e se surpreender. | `caso-terco-medio.jpg` |
| 04 | Bioestimuladores | A sua própria produção, reativada devagar. | Para quem perdeu firmeza e quer recuperar estrutura sem alterar a identidade. O resultado aparece de forma progressiva e natural. | `caso-frontal.jpg` |
| 05 | Anatomia facial | Cada medida lida antes de qualquer decisão. | Nariz, lábios e queixo são avaliados em conjunto, nunca como peças isoladas. É essa leitura completa que define o plano e a ordem das etapas. | `caso-mandibula.jpg` |
| 06 | Harmonização facial e corporal | Um plano desenhado para um rosto só — o seu. | A harmonização não é um produto: é a soma de decisões. Face e corpo são tratados em conjunto quando se completam. | `caso-panorama.jpg` |

**Publicar uma imagem depois — como fazer:** cada card já tem um `<div class="gcard__media">` reservado logo acima do texto, com a `<img>` comentada. Basta descomentar, apontar para `assets/caso-<slot>.jpg` (4:5) e apagar o comentário de instrução. Nada mais muda: nem o grid, nem a ordem, nem a altura dos cards vizinhos.

Por que funciona: `.gcard__media` tem `aspect-ratio:4/5` **sempre**, vazio ou não, e `object-fit:cover` no `img`. Como a altura do card já está prevista, inserir a foto não empurra o texto nem muda o alinhamento da linha. A versão anterior escondia a área com `:empty` e a expandia ao receber a imagem — o oposto do desejado. Estado vazio é um placeholder tracejado com ícone de câmera, para parecer proposital e não quebrado.

⚠️ `:empty` **não** casa quando o div tem quebra de linha ou espaço dentro. Comentários são ignorados, whitespace não. Como aqui o bloco é sempre visível, isso deixou de ser relevante — mas não usar `:empty` para ocultar por whitespace em outro lugar.

**Nota ética `.gal__note`** (abaixo dos cards, tracejado mais discreto)
> Quando houver imagens publicadas aqui, elas terão autorização por escrito, sem edição de cor ou forma e sem comparação de antes e depois. Os resultados variam de pessoa para pessoa conforme resposta biológica, técnica utilizada e indicações individuais.

CTA da seção: `Quero conhecer os protocolos` (`data-wa="anatomia"`)

### 4.5 A profissional

- Eyebrow: A profissional
- H2: **Dra. Thainá Lima**
- Lead: Biomédica esteta, conduz cada consulta partindo da escuta: do que incomoda você, do que faz você evitar fotos, do que você quer que notem.
- Bullets:
  - **Formação biomédica** aplicada a biossegurança e análise de contraindicações.
  - **Produtos certificados** e seleção rigorosa antes de qualquer indicação.
  - **Acolhimento**: você fala com quem atendeu, do início ao pós-procedimento.
  - **Honestidade** sobre o que é possível — e sobre o que não é.
- Credenciais: Biomedicina Esteta · Avaliação individualizada · Ética e biossegurança · Feira de Santana & Irará
- Pull quote: *O melhor resultado é o que continua parecendo você — só que mais presente.*
- Carimbo: **100%** Escuta antes
- CTAs: `Falar com a Dra. Thainá ou a equipe` + `Ver dúvidas frequentes`

### 4.6 Três passos, sem burocracia

| # | Título | Texto | CTA |
|---|---|---|---|
| 1 | Contato e pré-agendamento | Você chama no WhatsApp contando o que procura e onde prefere ser atendido(a). A equipe organiza os horários e confirma tudo em minutos. | `Iniciar meu pré-agendamento` |
| 2 | Avaliação presencial | Análise facial, medidas, fotos e conversa sobre o seu histórico. Você entende o que será feito e por quê. Sem compromisso de procedimento. | `Agendar minha avaliação` |
| 3 | Plano e execução | Você recebe um plano escrito, com prioridades, custos e cuidados. A execução acontece em etapas, com acompanhamento próximo. | `Entender meu plano` |

CTA de fechamento da seção: `Começar pelo passo 1 no WhatsApp`

**Ritmo:** gap título→passos 40px, gap passos→botão 22px. É a seção mais baixa da página (690px) de propósito — dá respiro depois da galeria.

### 4.7 Dúvidas frequentes

| Pergunta | Resposta (resumo) |
|---|---|
| Quanto tempo duram os resultados? | Varia por procedimento e organismo. Referência: toxina 4–6 meses; labial 12–18 meses; bioestimuladores de forma progressiva. A Dra. explica o caso real na consulta. |
| Dói? Precisa de anestesia? | Desconforto leve, ardor rápido de agulha. Anestésico tópico conforme a região. Técnica ajustada ao seu limiar; você pode pedir pausa. |
| Como é a recuperação? Posso trabalhar no mesmo dia? | Maioria retoma a rotina em poucas horas. Inchaço leve ou marcas discretas podem aparecer em 24–48h e são temporárias. |
| Botox deixa o rosto “congelado”? | Não, se dose e técnica forem calculadas corretamente. Rostos “congelados” indicam excesso de produto ou execução fora do plano. |
| Quanto custa? Como funciona a avaliação? | Depende do procedimento, volume e complexidade — por isso não publicamos tabela nem “promoção”. O plano com valores vem na avaliação. |
| Existe contraindicação? Preciso de encaminhamento? | Sim, avaliadas individualmente: gestação, aleitamento, alergias, anticoagulantes. Havendo necessidade, encaminhamos com todo cuidado. |

Bloco lateral **Tem outra dúvida?**
> Nenhuma pergunta é boba. Fale direto com a equipe no WhatsApp — respondemos com o mesmo cuidado da consulta, mesmo sem agendar.
> CTA: `Falar no WhatsApp` · Selo: Feira de Santana e Irará – BA

### 4.8 CTA final

- Eyebrow (gold): Seu próximo passo
- H2: **A versão mais bonita de você já existe. Ela só precisa de um olhar atento.**
- Sub: Uma conversa sem compromisso para entender o que incomoda você e o que faz sentido para a sua rotina. Escolha a cidade e agende direto.
- Botões: `Agendar em Feira de Santana` · `Agendar em Irará`
- Chips: Feira de Santana – BA / Atendimento presencial · Irará – BA / Atendimento presencial · WhatsApp / Resposta e agendamento

### 4.9 Rodapé

- Fecho: *“Sua imagem em harmonia com a sua identidade.”* Harmonização facial e corporal com avaliação individualizada e foco em naturalidade.
- Coluna **Atendimento**: Feira de Santana – BA · Irará – BA · Segunda a sábado, conforme agenda · Agendamento e dúvidas pelo WhatsApp
- Coluna **Navegação**: Filosofia · Procedimentos · Casos · A profissional · Dúvidas frequentes
- **Aviso legal e ético** (texto integral, ver §7)
- **Sigilo:** suas informações e fotos são utilizadas apenas para a avaliação do seu caso, com consentimento, e não são divulgadas.
- Linha de crédito: © {ano} Dra. Thainá Lima · Biomedicina Estética · Feira de Santana e Irará – BA

---

## 5. URLs parametrizadas

Base: `https://wa.me/557583527689?text={mensagem}`

> **Importante:** o link antigo `wa.me/message/27JA2QDLQFH7A1` faz 302 para `api.whatsapp.com/message/27JA2QDLQFH7A1` e **descarta o `?text=`**. Por isso a página usa o formato `wa.me/<número>?text=`.

### 5.1 Mapa `data-wa` (20 chaves, 22 links)

| Chave | Onde aparece | Mensagem decodificada |
|---|---|---|
| `topo` | Topbar, passo 1 (2×) | Olá! Vim pelo site e gostaria de iniciar meu pré-agendamento. |
| `hero` | CTA principal do hero | Olá! Vim pelo site da Dra. Thainá Lima e gostaria de agendar uma avaliação personalizada. |
| `cidadeFeira` | Link direto do hero | Olá! Vim pelo site e gostaria de saber informações sobre atendimento em Feira de Santana. |
| `cidadeIrara` | Link direto do hero | Olá! Vim pelo site e gostaria de saber informações sobre atendimento em Irará. |
| `objecao` | Callout da filosofia | Olá! Vim pelo site e gostaria de tirar uma dúvida sobre os procedimentos. |
| `perfilo` | Card 01 | Olá! Vim pelo site e gostaria de saber mais sobre Perfiloplastia. |
| `harmonizacao` | Card 02 | Olá! Vim pelo site e gostaria de saber mais sobre Harmonização Facial e Corporal. |
| `labial` | Card 03 | Olá! Vim pelo site e gostaria de saber mais sobre Preenchimento Labial natural. |
| `botox` | Card 04 | Olá! Vim pelo site e gostaria de saber mais sobre Toxina Botulínica (Botox). |
| `bioestim` | Card 05 | Olá! Vim pelo site e gostaria de saber mais sobre Bioestimuladores de Colágeno. |
| `anatomia` | CTA da galeria | Olá! Vim pelo site e gostaria de receber informações sobre protocolos e casos de tratamento. |
| `sobre` | CTA “A profissional” | Olá! Vim pelo site e tenho algumas dúvidas que gostaria de falar com a Dra. Thainá ou com a equipe. |
| `etapa1` | Passo 1 | Olá! Vim pelo site e gostaria de iniciar meu pré-agendamento. |
| `etapa2` | Passo 2 | Olá! Vim pelo site e gostaria de agendar uma avaliação presencial. |
| `etapa3` | Passo 3 | Olá! Vim pelo site e quero entender como será meu plano de tratamento. |
| `faq` | Bloco lateral do FAQ | Olá! Vim pelo site e minha dúvida não está na lista do FAQ. Podem me ajudar? |
| `finalFeira` | CTA final | Olá! Vim pelo site e gostaria de agendar uma avaliação em Feira de Santana. |
| `finalIrara` | CTA final | Olá! Vim pelo site e gostaria de agendar uma avaliação em Irará. |
| `rodape` | Link do rodapé | Olá! Vim pelo site e gostaria de falar com a equipe da Dra. Thainá Lima. |
| `flutuante` | Flutuante + barra mobile (2×) | Olá! Vim pelo site e gostaria de agendar uma avaliação com a Dra. Thainá Lima. |

### 5.2 Segmentação por cidade (runtime)

```js
var SUFIXO = {
  feira: ' Prefiro ser atendido(a) em Feira de Santana - BA.',
  irara: ' Prefiro ser atendido(a) em Irará - BA.'
};
```

Comportamento:
- Clicar em `[data-city]` anexa o sufixo a **todos** os `a[data-wa]`.
- Exceções preservadas (já são específicas de cidade): `cidadeFeira`, `cidadeIrara`, `finalFeira`, `finalIrara`.
- Clicar de novo na opção ativa desmarca e restaura o link original.
- `aria-pressed` reflete o estado; a mensagem do hint vira confirmação.

### 5.3 Exemplo montado

```
https://wa.me/557583527689?text=Ol%C3%A1!%20Vim%20pelo%20site%20e%20gostaria%20de%20saber%20mais%20sobre%20Perfiloplastia.%20Prefiro%20ser%20atendido(a)%20em%20Feira%20de%20Santana%20-%20BA.
```

---

## 6. Assets

### Fotos publicadas

| Arquivo | Origem em `img/` | Uso | Ratio | Export | Peso |
|---|---|---|---|---|---|
| `assets/dra-thaina-hero.jpg` | `1.jpg` | Hero | 4:5 | 1200×1500 | 241KB |
| `assets/dra-thaina-consulta.jpg` | `3.jpg` | A profissional | 3:4 | 1125×1500 | 162KB |
| `assets/dra-thaina-formacao.jpg` | `2.jpg` | Banda de formação | 4:5 | 900×1125 | 96KB |

O mapeamento foi confirmado por comparação de pixels: cada original foi reprocessado com o mesmo `centering` e comparado com o export publicado. A diferença média de luminância ficou em 0.03–0.10 para o par correto e 66–98 para os pares errados, então a associação acima não é suposição.

⚠️ A pasta `img/` é o **único backup dos originais em resolução cheia** — os exports em `assets/` já têm corte aplicado e não dá para recuperar o enquadramento completo. Manter versionada junto com o site.

Gerados com Pillow `ImageOps.fit`/LANCZOS, `quality=82`, `optimize+progressive`, `subsampling=0` (4:4:4, preserva tom de pele), sem EXIF.

Crops aplicados (fontes próximas do ratio alvo, perda pequena):

| Origem | Ratio | Alvo | Corte |
|---|---|---|---|
| `1.jpg` 1170×1463 | 0.800 | 4:5 | −3% de altura, `centering=(0.5, 0.30)` |
| `3.jpg` 1098×1372 | 0.800 | 3:4 | −2% de altura, `centering=(0.5, 0.50)` |
| `2.jpg` 978×1304 | 0.750 | 4:5 | −8% de altura, `centering=(0.5, 0.40)` |

O `centering` do hero é enviesado para cima de propósito: a foto é de corpo inteiro em pé, então o corte remove os pés e mantém o rosto na primeira dobra. Se o rosto ainda ficar pequeno demais no hero, subir para `(0.5, 0.15)` ou recortar o busto.

`img/` fica intacto como backup dos originais, em resolução cheia (1170×1463, 978×1304, 1098×1372).

### Slots disponíveis para casos reais

`assets/caso-{perfil,labial,terco-medio,frontal,mandibula,panorama}.jpg` — 4:5, sem uso no momento. Só publicar com autorização por escrito.

Sem arquivo no lugar, `onerror="this.remove()"` exibe o fallback `.ph__fb` automaticamente — a página nunca quebra.

### Referência de nomes

Os originais em `img/` estavam com os nomes-coluna do Instagram, contendo acentos e um `✨` (U+2728). Isso quebra em alguns hosts e em URLs. Os arquivos exportados usam nomes ASCII em minúsculas com hífen. Manter essa convenção.

### Ícone e PWA

Um único arquivo-fonte, `assets/favicon.svg`: círculo + eixo + ponto, tirados da ideia de avaliação milimétrica. Os PNGs saem dele por rasterização em potências de 2 (multiplicação inteira da base, sem reamostragem).

| Arquivo | Tamanho | Uso |
|---|---|---|
| `assets/favicon.svg` | 64×64 | Aba em navegadores modernos |
| `assets/favicon-32.png` | 32×32 | Fallback para navegadores antigos |
| `assets/apple-touch-icon.png` | 180×180 | iOS — precisa ser **opaco**: o iOS pinta preto o canal alpha |
| `assets/icon-192.png` | 192×192 | Android / manifesto |
| `assets/icon-512.png` | 512×512 | Tela de instalação |
| `assets/icon-maskable-512.png` | 512×512 | Android adaptativo, marca dentro da safe zone (80.9px de raio máx. contra 204.8px) |

`assets/site.webmanifest`: `display:standalone`, `theme_color:#1A1815`, `short_name:"Dra. Thainá"`.

Armadilhas que já custaram tempo aqui:

- **O nome no manifesto tem que bater com o arquivo.** O manifesto apontava `favicon-192.png` enquanto o arquivo gerado era `icon-192.png`: 404 silencioso, o navegador cai no ícone padrão e não reporta erro visível.
- **URLs do manifesto resolvem a partir do manifesto.** Como ele mora em `assets/`, escrever `assets/icon-512.png` resolve para `/assets/assets/...`. Use só o nome do arquivo, ou mova o manifesto para a raiz.
- **`start_url` e `scope` com `./`** apontam para `/assets/`, não para a raiz do site.
- **Valide por HTTP real, nunca por `file://`.** Em `file://` o `fetch` é bloqueado por CORS e falha em todos os recursos, gerando falso negativo em cascata.

No `<head>`: `viewport-fit=cover`, `theme-color` para esquema claro e escuro, `apple-mobile-web-app-status-bar-style`, `link[rel=icon]` apontando para SVG e PNG, `link[rel=apple-touch-icon]`, `link[rel=manifest]`.

---

## 7. Aviso legal (não resumir nem encurtar)

> Este site tem caráter exclusivamente informativo e não substitui a consulta ou a avaliação presencial com a Dra. Thainá Lima, biomédica esteta. Os procedimentos estéticos são realizados apenas após avaliação individual. Os resultados podem variar de pessoa para pessoa, conforme resposta biológica, técnica utilizada e cuidados no pós-procedimento. Não há promessa de resultado específico. Procedimentos são realizados somente quando há indicação clínica; contraindicações são avaliadas e, se necessário, o encaminhamento é feito.

⚠️ Nunca escrever "consulta médica" — a profissional é biomédica.

---

## 8. Checklist de publicação

**Resolvido**
- [x] Fotos do hero, A profissional e banda de formação exportadas em `assets/`
- [x] Galeria com 6 cards e area de imagem reservada 4:5 em cada slot (pronta para fotos futuras, sem alterar layout)
- [x] `figure{margin:0}` no reset — sem isso a banda perdia 80px de largura
- [x] BOM UTF-8 removido do início do `index.html`
- [x] Favicon + ícones de instalação + manifesto, todos resolvendo 200 por HTTP
- [x] Contraste WCAG AA (≥4.5:1) em 174 textos × 8 viewports, sem falhas
- [x] Sem overflow horizontal de 320px a 1440px
- [x] Alvos de toque ≥44px e microtextos ≥10.2px no mobile
- [x] Âncorasparam exatamente abaixo do topbar (delta 0) em desktop e mobile
- [x] Furo de navegação em 780–1019px fechado — a nav estava com estilo mas `display:none`
- [x] Botão flutuante não cobre mais a última linha do rodapé
- [x] Barra mobile medida em JS e publicada em `--mbar-h` (era 76px fixos,_media 87px)

**Pendente**
- [ ] Substituir `https://drathainalima.com.br/` pelo domínio real
- [ ] Conferir o enquadramento do rosto da foto do hero em 390px e 1440px
- [ ] Conferir visualmente o favicon em 16px, aba escura e home screen do Android
- [ ] Conferir se `apple-mobile-web-app-status-bar-style="black-translucent"` não atrapalha o topo em iPhone com notch
- [ ] Consentimento por escrito de cada paciente **antes** de descomentar qualquer `<img>` em `.gcard__media`
- [ ] Validar com a profissional as faixas de duração e as alegações de segurança
- [ ] Testar os 22 links com `?text=` em Android e iOS
- [ ] Confirmar que `wa.me/557583527689` abre a conversa com o texto colado
- [ ] Conferir que nenhum outro elemento usa `#25D366` além do flutuante
- [ ] `tools.new_image()` removido da configuração — não voltar a usar imagens geradas no lugar das fotos reais

---

## 9. Notas de verificação (leia antes de mexer no CSS)

Ferramentas de teste exigem HTTP de verdade, não `file://`. Um servidor local simples (`http.server`) na raiz do projeto resolve; o `file://` bloqueia `fetch` por CORS e faz todo recurso local parecer quebrado.

O Chrome headless recusa janelas menores que 500px em `set_window_size`. Para 320/360px, usar CDP:

```python
d.execute_cdp_cmd("Emulation.setDeviceMetricsOverride",
                  {"width":320,"height":568,"deviceScaleFactor":2,"mobile":True})
```

Erros que os testes ducked, e que voltam a aparecer se a checagem for frouxa:

- **Contraste em fundo transparente.** Compor `rgba(255,255,255,.05)` sobre um gradiente escuro exige empilhar as camadas do ancestral mais externo para dentro. Compor sobre branco gera contraste falso de 1.12 em `.btn-light`, que passa na auditoria e reprova no olho.
- **Media query no limite exato.** `min-width:1040px` testado em "1040px" pode cair fora da faixa se o `innerWidth` efetivo for outro. Confirmar `matchMedia(...).matches` no próprio navegador.
- **Hover precisa de hover de verdade.** `ActionChains.move_to_element` reproduz o `:hover`; injetar uma classe de hover não reproduz o cascade e mascara bug de ordem de regra.
- **Scroll suave.** `scrollTo` com `scroll-behavior:smooth` não chega ao fim antes de a medição; desativar temporariamente e rolar duas vezes antes de ler.
- **`imgs=2/3` não é imagem quebrada.** `loading="lazy"` fora da viewport é o comportamento esperado. Confirmar rolando a página inteira.

Ordem obrigatória das regras de toque: o `.card:hover` vem **depois** do `.card--lead` de propósito. Mesma especificidade (0,2,0), então a ordem decide. Fora de `min-width:1040px` o card lead é claro com texto escuro e não deve herdar o gradiente.