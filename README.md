# CSS

## <a id="sumario">Sumário</a>

- [Fundamentos](#fundamentos)
  - [1. Seletores](#seletores)
  - [2. Seletores combinados](#seletores-combinados)
  - [3. Dimensionamento e espaçamento](#dimensionamento-e-espacamento)

- [Complementar](#complementar)

## <a id="fundamentos">Fundamentos</a> [[sumário]](#sumario)

### <a id="seletores">1. Seletores</a>

Tipo | Modelo
:-: | ---
Tag / Tipo | h1 {} 
Id | #id {} 
Classe | .class {} 
Universal | * {} 
Atributo | [atributo] {} 
Atributo com valor | [atributo="valor"] {} 

[Complementar: seletores por atributo](#seletores-por-atributo)

## <a id="seletores-combinados">2. Seletores combinados</a>

Tipo | Modelo
:---: | ---
Separados por vírgula | h1, #id, .class {} 
Seletor específico | h1.class {} 
Descendente | div h1 {} 
Filho | div > p {} 
Irmão adjacente | h2 + p {} 
Irmão geral | h2 ~ p {} 

[Complementar: combinadores](#combinadores)

## <a id="dimensionamento-e-espacamento">3. Dimensionamento e espaçamento</a>

Propriedades:

- `width`
- `height`
- `max-width` e `min-width`
- `max-height` e `min-height`
- `margin` (`shorthand`)
- `padding` (`shorthand`)
- `box-sizing`

Obs.: `shorthand` é uma forma abreviada

Outras:

- `margin-top`, `margin-left`, `margin-right` e `margin-bottom`
- `padding-top`, `padding-left`, `padding-right` e `padding-bottom`

Regra das `shorthands` de espaçamento (`margin` e `padding`):

- `margin: 10px;` -> 10px (cima, baixo, laterais)
- `margin: 5px 10px;` -> 5px (cima e baixo), 10px (laterais)
- `margin: 5px 10px 20px;` -> cima, lados, baixo
- `margin: 5px 10px 15px 8px;` -> cima, direita, baixo, esquerda
- Obs.: pode-se utilizar valores negativos







## <a id="complementar">Complementar</a>

### <a id="seletores-por-atributo">Seletores por atributo</a>

Tipo | Modelo
:---: | ---
Atributo separado por espaço | [atributo~="valor"] {} 
Atributo separado por hífen | [atributo\|="valor"] {} 
Atributo por pre-fixo | [atributo^="valor"] 
Atributo por sufixo | [atributo$="valor"] 
Atributo por qualquer lugar | [atributo*="valor"] 

### <a id="combinadores">Combinadores</a>

Descendente

```css
div p {
  color: blue;
}
```

```html
<div>
  <p>Este parágrafo será azul.</p>
  <span><p>Este parágrafo também será azul, mesmo não sendo um filho direto do div.</p></span>
</div>
```

Filho

```css
div > p {
  color: blue;
}
```

```html
<div>
  <p>Este parágrafo será azul.</p>
  <span><p>Este parágrafo não será azul, pois não é um filho direto do div.</p></span>
</div>
```

Irmão adjacente

```css
h2 + p {
  color: green;
}
```

```html
<h2>Título</h2>
<p>Este parágrafo será verde.</p>
<p>Este parágrafo não será afetado.</p>
```

Irmão geral

```css
h2 ~ p {
  color: green;
}
```

```html
<h2>Título</h2>
<p>Este parágrafo será verde.</p>
<p>Este parágrafo também será verde.</p>
```



