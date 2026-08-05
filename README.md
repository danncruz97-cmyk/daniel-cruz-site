# Landing page — Daniel Cruz

Site de página única, sem framework e sem build. É HTML, CSS e JavaScript em
um arquivo só (`index.html`) mais a pasta `assets/`. Abre no navegador com
duplo clique e publica em qualquer hospedagem estática.

---

## Rodar na sua máquina

Duplo clique em `index.html` já funciona. Se quiser servir localmente
(recomendado, porque alguns navegadores bloqueiam arquivos locais):

```bash
# Python (já vem instalado no Mac e no Linux)
python3 -m http.server 8000
# depois abra http://localhost:8000

# ou com Node
npx serve
```

---

## Estrutura

```
.
├── index.html                    ← a página inteira: HTML + CSS + JS
├── robots.txt                    ← trocar SEU-DOMINIO
├── sitemap.xml                   ← trocar SEU-DOMINIO e a data
└── assets/
    ├── img/
    │   ├── daniel-cruz.jpg           foto do Sobre (em uso)
    │   ├── daniel-cruz-fechado.jpg   corte alternativo, mais aproximado
    │   ├── daniel-cruz.webp          mesma foto, formato leve
    │   ├── projeto-luis-desktop.webp print do projeto do Dr. Luis Eduardo no card
    │   ├── projeto-campus-copy-desktop.png print do projeto da Campus Copy no card
    │   ├── projeto-allyson-desktop.png print do projeto do Benício Advogados no card
    │   └── projeto-allysson-mobile2.png print do escritório Benício no celular do hero
    ├── logo/
    │   ├── dc-simbolo.svg            símbolo (em uso no cabeçalho)
    │   ├── dc-simbolo-branco.svg     fundo escuro
    │   ├── dc-simbolo-preto.svg      uma cor: carimbo, gravação
    │   ├── dc-favicon.svg            aba do navegador (em uso)
    │   ├── dc-logo-horizontal.svg    assinatura de e-mail, cabeçalhos
    │   ├── dc-logo-empilhado.svg     redes sociais, cartão
    │   └── png/                      as mesmas em PNG transparente
    └── docs/
        └── dc-especificacao.md       manual da marca: cores, medidas, regras
```

---

## O que trocar antes de publicar

### 1. WhatsApp
Está em **uma linha só**, no início do `<script>`, no fim do `index.html`:

```js
const WHATSAPP_NUMERO = '5574981301345';
```

Os 12 botões da página puxam desse único lugar, cada um com uma mensagem
pré-preenchida diferente (definida no atributo `data-msg` de cada botão).

### 2. Domínio
Procure por `SEU-DOMINIO` em `robots.txt` e `sitemap.xml` e substitua.

### 3. Domínios dos projetos
Os três cards de projeto da seção **Projetos** apontam para:

- `https://www.luiseduardoadv.com.br/` (Dr. Luis Eduardo, 1º card)
- `https://campus-copy-landing-page.vercel.app/` (Campus Copy, 2º card)
- `https://drallyssonbenicio.vercel.app/` (Benício Advogados, 3º card)

Confirme que os três estão no ar antes de publicar, porque a página anuncia
todos como "No ar" e o visitante vai clicar.

### 4. Depoimentos reais
A seção de depoimentos está **guardada comentada** no HTML (procure por
`DEPOIMENTOS — GUARDADO PARA QUANDO VOCÊ TIVER OS REAIS`), já pronta para
ativar: o grid se adapta sozinho a 1, 2 ou 3 depoimentos. Quando tiver as
frases verdadeiras, siga as instruções no próprio comentário — isso inclui
remover a tira "E estou começando agora" da seção "Sobre" (`.about__soon`)
e reconferir a alternância de fundos branco/cinza das seções abaixo.

### 5. Garantia
A seção "Como eu tiro o risco da sua mão" promete 50/50, aprovação antes
de publicar e uma refação inclusa. **Confirme que você consegue cumprir os
três** antes de deixar no ar. Garantia não honrada é pior que garantia
nenhuma.

---

## Como adicionar um projeto novo

Na seção `PROJETOS REALIZADOS`, copie um bloco inteiro
`<a class="proj-card"> ... </a>` e cole abaixo. Existe um modelo comentado
logo depois do card de chamada ("Seu projeto pode ser o próximo"), pronto
para preencher — cole seu novo card antes dele, para o card de chamada
continuar por último.

O carrossel se ajusta sozinho:

| Projetos | Comportamento |
|---|---|
| 1 | card único centralizado, sem controles |
| 2 | lado a lado, com setas e indicadores |
| 3 ou mais | carrossel com swipe no celular |

Não esqueça de atualizar o contador da seção (`<span class="counter"><b>3</b>`)
e a frase do bloco "Seu segmento não está aqui?", que cita os segmentos já
atendidos por nome.

---

## Publicar

Qualquer uma serve, todas com plano gratuito:

**GitHub Pages** — Settings → Pages → Branch `main` → `/root`.
Sai em `https://usuario.github.io/repositorio`.

**Vercel** ou **Netlify** — conecte o repositório e faça deploy. Sem
configuração, porque não há build. Domínio próprio nas configurações.

Depois de apontar o domínio, atualize `robots.txt` e `sitemap.xml`.

---

## Decisões que valem manter

**Verde é ação.** `#25D366` só em botão que leva ao WhatsApp. Nunca na
logo, nunca em decoração. É o que faz o verde significar algo.

**Marinho é a marca.** `#1E3A8A` em títulos, ícones e no símbolo.

**Sem localStorage.** Se você for editar com IA, saiba que a página não
usa nem precisa de armazenamento no navegador.

**Movimento reduzido respeitado.** Há um bloco
`@media (prefers-reduced-motion: reduce)` que desliga as animações para
quem configurou isso no sistema. Não remova.

**Acessibilidade.** Foco visível no teclado, `aria-expanded` no menu e no
FAQ, `alt` em todas as imagens. Ao adicionar seção, mantenha o padrão.

---

## Paleta

| Uso | Hex |
|---|---|
| Marinho da marca | `#1E3A8A` |
| Texto | `#0F172A` |
| Texto secundário | `#475569` |
| Fundo alternado | `#F9FAFB` |
| Bordas | `#E6EAF1` |
| Ação, WhatsApp | `#25D366` |

Tipografia: **Plus Jakarta Sans** nos títulos, **Inter** no texto.
A Fraunces e a Cormorant Garamond são carregadas apenas para a prévia do
projeto do Benício no carrossel.
