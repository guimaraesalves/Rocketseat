# Comentários

* Não irá afetar o seu código
* Ajuda a lembrar blocos de códigos
* Deixa dicas para leitura
* Ajuda outros a entendenrem
* Nunca esqueça de fechar um comentário aberto

Comentários começam com `/*` e terminam com `*/`.

```css

/* Básico */
/* --------------------------------- */
```

# Anatomia

```css
h1 {
    color: blue;
    font-size: 60px;
    background: gray;
}
```
* Selector
* Declaration
* Properties
* Property Value


# Selectors

Conecta um elemento HTML com o CSS

## Tipos

* Global selector `*`
* Element/Type selector `h1, h2, p, div`
* ID Selector `#box, #container`
* Class Selector `.red, .m-4`
* Attribute selector, Pseudo-class, Pseudo-element, e outros.

# Caixas

* Você irá perceber que (quase) tudo são caixas do CSS
* Posicionamentos, tamanhos, espaçamentos, bordas, cores
* Caixa pode ficar ao lado uma da outra, ou acima
* Elementos HTMl são caixas


# Adicionando CSS

## inline

* atributo `style`

## `<style>`

* tag html que irá conter o css

## `<Link>`
* arquivo css externo

## @import
* arquivo css externo

# A Cascata (cascading)
A escolha do brower de qual regra aplicar, caso haja muitas regras para o mesmo elemento.

* Seu estilo é lido de cima para baixo.

É levado em consideração 3 fatores

1. Origem do estilo
2. Especificidade
3. Importância

### Origem do estilo

inline > tag style > tag link

### Especificidade

É um cálculo matemático, onde, cada tipo de seletor e origem do estilo, possuem valores a serem considerados.

0 -  Universal selector, combinators e nagation pseudo-class (:not())

1 - Element type selector e pseudo-elements (::before, ::after)

10 - Classes e attribute selectors ([type="radio"])

100 - ID selector

1000 - Inline

### A regra !important
* Cuidado, evite o uso
* Não é considerado uma boa prática
* Quebra o fluxo natural da cascata


# At-rules

* Está relacionado ao comportamento do CSS
* Começa com o sinal de `@` seguido do identificador e valor

## Exemplos comuns

- @import --> /* incluir um CSS externo */

- @media --> /* regras condicionais para dispositivos */

- @font-face --> /* fontes externas */

- @keyframes --> /* Animation */

```css
@import "http://local.com/style.css;

@media (min-width: 500px) {
    /* rules here */
}

@font-face {
    /* rules here */
}

@keyframes nameofanimation {
    /* rules here */
}

```

# Shorthand

* Junção de propriedades
* Resumido
* Legível

```css
{
    /* background properties */
    background-color: #000;
    background-image: url(images/bg.gif);
    background-repeat: no-repeat;
    background-position: left top;

    /* background shorthand */
    background: #000 url(images/bg.gif) no-repeat left top;

    /* font properties */
    font-style: italic;
    font-weight: bold;
    line-height: 1.2;
    font-family: Arial, sans-serif;

    /* font shrthand */
    font: italic bold .8em/1.2 Arial, sans-serif;
}
```
## Detalhes

* Não irá considerar propriedades anteriores
* Valores não especificados irão assumir o valor padrão
* geralmente, a ordem descrita não importa, mas, se houver muitas propriedades com valores semelhantes, poderemos encontrar problemas

## Propriedades que aceitam shorthand

animation, background, border, border-bottom, border-color, border-left, border-radius, border-right, border-style, border-top, border-width, column-rule, columns, flex, flex-flow, font, grid, grid-area, grid-column, grid-row, grid-template, list-style, margin, offser, outline, overflow, padding, place-content, place-items, place-self, text-decoration, transition

**https://developer.mozilla.org/en-US/docs/Web/CSS/Shorthand_properties**

# Funções

* nome seguido de abre e fecha parentesis
* recebe argumentos (valores entre parênteses)

## Exemplos
```css
@import url("http://urlaqui.com/style.css");

{
    color: rgb(255, 0, 100);
    width: calc(100% - 10px);
}
```

# DevTools

F12 --> no Browser

# Cuidados com a escrita
formatando o texto corretamente através dos espaços, identação, hiffens e etc...


# Vendor prefixes

Permite que browsers adicione `features` a fim de colocar em uso alguma novidade que vemos no CSS

# Exemplo

```css
p {
    -webkit-background-clip: text;
    -moz-background-clip: text;
    -ms-background-clip: text;
    -o-background-clip: text;
}
``` 
**-webkit-** *vendor prefixes* do:  Chrome, Safari, iOS e Android

**-moz-** *vendor prefixes*: Mozilla (firefox)

**-ms-** *vendor prefixes*: Internet Explorer

**-o-** *vendor prefixes*:Opera

# Consultas
[https://ireade.github.io/which-vendor-prefix/]
[http://caniuse.com]












