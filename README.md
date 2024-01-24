# CSS

---

## <a id="sumario">Sumário</a>

- [1. Fundamentos](#fundamentos)
  - [1.1. Seletores](#seletores)
  - [1.2. Seletores combinados](#seletores-combinados)
  - [1.3. Dimensionamento e espaçamento](#dimensionamento-e-espacamento)

- [2. Estilizações](#estilizacoes)
  - [2.1. Cores](#cores)
  - [2.2. Imagens](#imagens)
  - [2.3. Fundo dos elementos](#fundo-dos-elementos)
  - [2.4. Bordas](#bordas)

- [x. Complementar](#complementar)





---

## <a id="fundamentos">1. Fundamentos</a> [[sumário]](#sumario)

### <a id="seletores">1.1. Seletores</a>

Tipo | Modelo
:-: | ---
Tag / Tipo | h1 {} 
Id | #id {} 
Classe | .class {} 
Universal | * {} 
Atributo | [atributo] {} 
Atributo com valor | [atributo="valor"] {} 

[Complementar: seletores por atributo](#seletores-por-atributo)

### <a id="seletores-combinados">1.2. Seletores combinados</a>

Tipo | Modelo
:---: | ---
Separados por vírgula | h1, #id, .class {} 
Seletor específico | h1.class {} 
Descendente | div h1 {} 
Filho | div > p {} 
Irmão adjacente | h2 + p {} 
Irmão geral | h2 ~ p {} 

[Complementar: combinadores](#combinadores)

### <a id="dimensionamento-e-espacamento">1.3. Dimensionamento e espaçamento</a>

Propriedades:

- `width`
- `height`
- `max-width` e `min-width`
- `max-height` e `min-height`
- `margin` (`shorthand`)
- `padding` (`shorthand`)
- `box-sizing`

Obs.: `shorthand` é uma forma abreviada de escrever várias outras propriedades.

Outras:

- `margin-top`, `margin-left`, `margin-right` e `margin-bottom`
- `padding-top`, `padding-left`, `padding-right` e `padding-bottom`

<a id="regra-mais-de-um-valor">Regra das `shorthands`</a> de espaçamento (`margin` e `padding`):

- `margin: 10px;` -> 10px (cima, baixo, laterais)
- `margin: 5px 10px;` -> 5px (cima e baixo), 10px (laterais)
- `margin: 5px 10px 20px;` -> cima, lados, baixo
- `margin: 5px 10px 15px 8px;` -> cima, direita, baixo, esquerda
- Obs.: pode-se utilizar valores negativos

---

## <a id="estilizacoes">2. Estilizações</a> [[sumário]](#sumario)

### <a id="cores">2.1. Cores</a>

Tipo | Modelo
:---: | ---
Pré-definidas | blue 
Cor atual da propriedade color | currentcolor 
Transparente | transparent 
RGB | rgb(n, n, n) 
RGBA | rgba(n, n, n, n) 
Hexadecimal | #rrggbb 
Hexadecimal com transparência | #rrggbbaa 
HSL | hsl(n, n, n) 
HSLA | hsla(n, n, n, n) 

[Complementar: tipos de valores em cores](#tipos-de-valores-em-cores)

### <a id="imagens">2.2. Imagens</a>

`object-fit`:

Valor | Descrição
:---: | ---
fill | distorce a imagem 
contain | ocupa o máximo de espaço sem distorcer 
cover | recorta a imagem, ocupando todo o espaço do contâiner 
none | mantém o tamanho original da imagem 
scale-down | escolhe a configuração que a imagem fica menor 

`object-position: valor-1 valor-2`

- valor-1 (eixo horizontal): aceita os valores `left`, `center` e `right`
- valor-2 (eixo vertical): aceita os valores `top`, `center` e `bottom`

### <a id="fundo-dos-elementos">2.3. Fundo dos elementos</a>

`background-color: cor`

`background-image`:

Valor | Descrição
:---: | ---
url('caminho-da-imagem') | Adiciona uma imagem 
linear-gradient(cor1, cor2, ...) | Adiciona um gradiente linear 
radial-gradient(cor1, cor2, ...) | Adiciona um gradiente radial 
repeting-linear-gradient(to top ...) | O gradiente se repete 
url('url-img-1'), url('url-img-2') | Adiciona camadas de imagens 

`background-size`:

Valor | Descrição
:---: | ---
auto | Ajusta automaticamente 
cover | Redimensiona para cobrir todo o contâiner 
contain | Redimensiona para imagem aparecer completamente 
12px | Define a largura em pixels ou em porcentagem 
12px 5px | Define a largura e altua respectivamente 
cover, 5px | Redimensiona as camadas respectivamente 

`background-repeat`:

Valor | Descrição
:---: | ---
repeat | A imagem se repete lado a lado em todas as direções 
repeat-x | A imagem se repete apenas no eixo x 
repeat-y | A imagem se repete apenas no eixo y 
space | A imagem se repete em todas as direções com um espaço entre elas 
round | redimensiona a imagem para caber as repetições 
no-repeat | A imagem não se repete 
repeat space | Define para os x e y respectivamente 

`background-position`:

Valor | Descrição
:---: | ---
top | Ajusta a imagem ao topo 
bottom | Ajusta a imagem abaixo 
right | Ajusta a imagem à direita 
left | Ajusta a imagem à esquerda 
center | Ajusta a imagem ao centro 
top 12px | Ajusta a imagem à 12px do topo, aceita porcentagem 
top right | Ajusta a imagem ao topo e à direita simultaneamente 
top, right | Ajusta as camadas da imagem respectivamente 

`background-attachment`:

Valor | Descrição
:---: | ---
fixed | Imagem fica fixa na página 
scroll | Imagem se move junto com a página principal 
local | Imagem se move junto com o elemento local 

`background-origin`:

Valor | Descrição
:---: | ---
padding-box | Imagem cobre a área do padding 
border-box | Imagem cobre a borda 
content-box | Não cobre o padding, só a área do conteúdo 

`background-clip`:

Valor | Descrição
:---: | ---
" " | Mesmos valores que `background-origin` 
text | Preenche a cor do texto com a imagem de fundo 

Obs.: para o valor `text` funcionar utilize os comandos

```css
seletor {
    -webkit-background-clip: text;
	color: transparent;
	background-clip: text;
}
```

`background-blend-mode`: existem muitos valores possíveis

Obs.: para esse comando funcionar corretamente, adicione uma cor de fundo para que ela possa se mesclar com a imagem

`background` (shorthand):

- `background-color`
- `background-image`
- `background-repeat`
- `background-attachment`
- `background-position`

### <a id="bordas">2.4. Bordas</a>

`border-width`:

Valor | Descrição
:---: | ---
thin | Borda padronizada fina 
medium | Borda padronizada média 
thick | Borda padronizada grossa 
12px | Valor com unidade de medida 
5px ... | Mais de um valor segue a mesma regra do [`margin`](#regra-mais-de-um-valor) 

`border-style`:

Valor | Descrição
:---: | ---
dashed | Borda com linhas pontilhadas 
dotted | Borda pontilhada 
double | Borda com duas linhas retas 
groove | Borda com aparência esculpida 
ridge | Borda com aparência extrudada 
inset | Borda que faz o elemento parecer incorporado 
outset | Borda que faz o elemento parecer em relevo 
12px | Borda com um valor com unidade de medida 
5px ... | Mais de um valor segue a mesma regra do [`margin`](#regra-mais-de-um-valor) 

`border-color`:

Valor | Descrição
:---: | ---
blue | cor para todas as boras 
blue red ... | Mais de um valor segue a mesma regra do [`margin`](#regra-mais-de-um-valor) 

`border-radius`:

Valor | Descrição 
:---: | ---
12px | Arredonda as bordas 
5px ... | Mais de um valor segue a mesma regra do [`margin`](#regra-mais-de-um-valor) 
5px/12px | Bordas horizontais e verticais respectivamente 
50% | Valores em porcentagem, 50% vira um círculo 

A propriedade `border` é uma shorthand, assim como `border-top`, `border-bottom`, `border-left` e `border-right`, usando a sequência:

- `border-width`
- `border-style` (required)
- `border-color`

Obs.: por serem shorthands, propriedades como `border-bottom-width` também são válidas.

[Complementar: bordas com imagem](#bordas-com-imagem)







---

## <a id="complementar">x. Complementar</a> [[sumário]](#sumario)

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

### <a id="tipos-de-valores-em-cores">Tipos de valores em cores</a>

- RGB: `rgb(0-255, 0-255, 0-255)`
  - ou `rgb(0-100%, 0-100%, 0-100%)`
- RGBA: `rgba(0-255, 0-255, 0-255, 0.0-1.0)`
- Hexadecimal: `#rrggbb`
- Hexadecimal com transparência: `#rrggbbaa`
- HSL: `hsl(0-360, 0-100%, 0-100%)`
  - Hue (matiz): 0 a 360
  - Saturation (saturação): 0 a 100%
  - Lightness (luminosidade): 0 a 100%
- HSLA: `hsla(0-360, 0-100%, 0-100%, 0.0-1.0)`

### <a id="bordas-com-imagem">Bordas com imagem</a>

#### Propriedade border image source

- border-image-source: url('caminho-da-imagem') -> ou gradiente

#### Propriedade border image slice

- border-image-slice: valor
- border-image-slice: valor fill -> preenche o centro, a parte do conteúdo

#### Propriedade border image width

- border-image-width: valor
- border-image-width: valor1 valor2
  - demais casos para mais de um valor

#### Propriedade border image repeat

- border-image-repeat: valor
  - repeat -> repete a image para preencher o espaço
  - stretch -> distorcer a imagem menos os cantos
  - round -> redimensiona a imagem e evita cortar a imagem
  - space -> redimensiona a imagem e adiciona um espaço entre elas
- border-image-repeat: valor1 valor2
  - demais casos para mais de um valor

#### Propriedade border image outset

- border-image-outset: valor -> distância da borda
- border-image-outset: valor1 valor2
  - demais casos para mais de um valor

#### Propriedade border image

- border-image: valor1 valor2 ...
