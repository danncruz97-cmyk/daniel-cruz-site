# Marca Daniel Cruz — especificação

## Cor

| Uso | Hex | RGB |
|---|---|---|
| Marinho da marca | `#1E3A8A` | 30, 58, 138 |
| Tagline | `#475569` | 71, 85, 105 |
| Verde de ação (botões, **nunca na marca**) | `#25D366` | 37, 211, 102 |

O verde pertence aos botões. Na marca ele deixa de ser sinal de "clique aqui"
e passa a ser decoração.

## Geometria do símbolo

Caixa de **425 × 440** (proporção 0,966).

| Elemento | Medida |
|---|---|
| Espessura do traço (uniforme) | 50 |
| Anel branco entre D e C | 40 nos lados retos, 35 a 55 junto à curva |
| Contraforma do C | 130 × 160 |
| Abertura do C | 80 (centrada na altura) |
| Raio dos cantos internos | 10 |
| Raio do bojo externo do D | 150 |

O anel é mais largo junto à curva de propósito: espaço entre reta e curva
parece menor do que mede.

## Tipografia

**Nome** — Plus Jakarta Sans ExtraBold (800), entreletra −2%, `#1E3A8A`
**Tagline** — Plus Jakarta Sans Medium (500), entreletra +8%, `#475569`,
corpo a **32% do nome**

O corpo de 32% não é arbitrário: é o valor que faz o tagline ter exatamente
a mesma largura do nome. As duas linhas alinham por dimensionamento, nunca
por esticar ou comprimir o texto.

Nos arquivos de conjunto o texto já está convertido em contornos. Não
depende de fonte instalada e não vai se deformar em nenhum lugar.

## Área de respiro

Reserve em volta da marca uma margem igual a **um quinto da altura** do
símbolo. Nada entra nessa faixa.

## Tamanhos mínimos

| Aplicação | Mínimo |
|---|---|
| Símbolo isolado | 16 px (testado, o anel branco se mantém) |
| Conjunto horizontal | 120 px de largura |
| Conjunto empilhado | 90 px de largura |

Abaixo de 24 px use `dc-favicon.svg`, que tem traço e anel mais grossos.

## Arquivos

| Arquivo | Uso |
|---|---|
| `dc-simbolo.svg` | símbolo em marinho, uso principal |
| `dc-simbolo-branco.svg` | fundo escuro |
| `dc-simbolo-preto.svg` | uma cor: carimbo, gravação, fax, jornal |
| `dc-favicon.svg` | aba do navegador, ícone de app, avatar |
| `dc-logo-horizontal.svg` | cabeçalho de site, assinatura de e-mail |
| `dc-logo-empilhado.svg` | perfil de rede social, cartão, formatos estreitos |

## Verificação feita

| Teste | Resultado |
|---|---|
| Cor renderizada | `#1E3A8A` exato |
| Traço, mediana | 49,9 (desvio 1,28) |
| D e C separados a 48, 32, 24 e 16 px | sim, nos quatro |
| Branco do anel a 16 px | 255, preservado |
| Largura nome × tagline | 528,1 × 528,1 |
| Centralização do bloco de texto | 0 px de desvio |
| Glifos legíveis no tagline | 24 de 24 |

## O que não fazer

Esticar ou condensar o texto. Aplicar degradê. Trocar o marinho por outro
azul. Colocar o símbolo dentro de outra forma. Rotacionar. Adicionar sombra
ou brilho. Usar o verde no símbolo.
