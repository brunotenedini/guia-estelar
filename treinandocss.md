# Introdução

## O que significa CSS ?

* Cascading Style Sheet (Folha de Estilo em Cascata)
* Código para criar estilos no HTML
* HTML é a estrutura, o CSS é a beleza
* Não é uma linguagem de programação
* É uma linguagem style sheet

## Vamos ao exemplo

# Comentários

* Não irá afetar o seu código
* Ajuda a lembrar blocos de códigos
* Deixa dicas para leitura
* Ajuda outros a entenderem
* Nunca esqueça de fechar um comentário aberto

Comentários começam com `/*` e terminam com `*/`.

```css
/* Básico */
/* ------------------*/
```

* Você poderá usar para desabilitar partes do seu código
```css

/*.special { color: red;}*/
```

# Anatomia

```css
h1 {                        h1= selector
    color: blue;            color= (declaration) propriedade  blue= valor
    font-size: 60px;        font-size= (declaration) propriedade   60px= valor
    background: gray;       background= (declaration) propriedade  gray= valor

}
```

* Selector
* Declaration
* Properties
* Protperty Value

# Selectors

Conecta um elemento HTML com o CSS

## Tipos

* Global selector `*`
* Element/Type selector `h1, h2, p, div`
* ID Selector `#box, #container`
* Class Selector `.red, .m-4`
* Attribute selector, Pseudo-class, Pseudo-element, e outros

# Caixas

* Altura e largura
* Espaços, espaços entre as caixas

# Adicionando CSS

## inline

* atributo`style`

## <style>
 
* tag html irá conter o css 

## <link>

* arquivo css externo

## @import

* arquivo css externo

# A Cascata (cascading)

A escolha do browser de qual regra aplicar, caso haja muitas regras para o mesmo elemento.

* Seu estilo é lido de cima para baixo.

È levado em consideração 3 fatores 

1. Origem do estilo
2. Especificidade
3. Importância

### Origem do estilo
```css
 /* (<h1 style>) (<style></style>) (css) porém continua de cima pra baixo */
```
inline  >  tag style   >   tag link

### Especificidade

È um cálculo matemático, onde, cada tipo de seletor e origem do estilo, possuem valores a serem considerados.

```css
/* 
    0= *   1= ex: h1  10= class  100= id#
*/
```
0. Universal selector, combinators e negation pseudo-class (:not())
1. Element type selector e pseudo-elements (::before, ::after)
10. Classes e attribute selectors ([type="radio"])
100. ID selector
1000. Inline

### A regra !important

* cuidado, evite o uso
* não é considerado uma boa prática
* quebra o fluxo natural da cascata

# At-rules

* Está relacionado ao comportamento do CSS
* Começa com o sinal de `@` seguido do identificador e valor

## Exemplos comuns

```css

- @import  /* incluir um CSS externo  */ 

- @media    /* regras condicionais para dispositivos */

- @font-face  /* fontes externas */

- @keyframes  /* animation */

```

# Shorthand

* junção de propriedades
* resumido
* legível

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
    font-size: .8em;
    line-height: 1.2;
    font-family: Arial, sans-serif;

    /* font shorthand */
    font: italic bold .8em/1.2 Arial, sans-serif;

}
```

## Detalhes

* não irá considerar propriedades anteriores
* valores não especificados irão assumir o valor padrão 
* geralmente, a ordem descrita não importa, mas, se houver muitas propriedades com valores semelhantes, poderemos encontrar problemas

**https://developer.mozilla.org/en-US/docs/Web/CSS/Shorthand_properties**

# Funções

* nome seguido de abre e fecha parentesis
* recebe argumentos

## Exemplos

```css
@import url("http://urlaqui.com/style.css"):

{
    color: rgb(255, 0, 100);
    width: calc(100% - 10px);
}

```

# Vendor Prefixes

Permite que browsers adicionem `features`
a fim de colocar em uso alguma novidade que vemos no CSS

## Exemplo

```css
p {
    -webkit-background-clip: text;   /* Chrome. Safari, iOS e Android */
    -moz-background-clip: text;     /* Mozilla (firefox) */
    -ms-background-clip: text;      /* Internet Explorer */
    -o-background-clip: text;       /* Opera */
}
```

# Consultas

.[http://ireade.github.io/which-vendor-prefix/].
.[http://caniuse.com].







