# Resumo CSS: Estilização Básica

## Cores
- **Pré-definidas:** `red`, `blue`, `green`, etc.
- **RGB:** `rgb(255, 0, 0)` (vermelho)
- **RGBA:** `rgba(255, 0, 0, 0.5)` (vermelho com transparência)
- **Hexadecimal:** `#FF0000` (vermelho)
- **HSL:** `hsl(0, 100%, 50%)` (vermelho)
- **HSLA:** `hsla(0, 100%, 50%, 0.5)` (vermelho com transparência)

## Imagens e Objetos
- **object-fit:** Controla como a imagem se ajusta ao container (`cover`, `contain`, `fill`, etc.)
- **object-position:** Define o posicionamento da imagem dentro do container (`center`, `top`, `left`, etc.)

## Fundo dos Elementos
- **Alterar fundo:** `background-color`, `background-image`
- **Redimensionar imagem de fundo:** `background-size: cover | contain | auto`
- **Repetição:** `background-repeat: repeat | no-repeat | repeat-x | repeat-y`
- **Posicionamento:** `background-position: center | top | left | valores em px ou %`
- **background-attachment:** `scroll | fixed | local`
- **background-origin:** Define área de origem do fundo (`border-box`, `padding-box`, `content-box`)
- **background-clip:** Define até onde o fundo se estende (`border-box`, `padding-box`, `content-box`)
- **background-blend-mode:** Mescla o fundo com cor ou imagem (`multiply`, `screen`, etc.)
- **Propriedade resumida:** `background: color image position/size repeat origin clip attachment;`

## Bordas
- **Tamanho:** `border-width: 2px`
- **Estilo:** `border-style: solid | dashed | dotted`
- **Cor:** `border-color: #000`
- **Propriedade resumida:** `border: 2px solid #000`
- **Arredondamento:** `border-radius: 10px`
- **Imagem na borda:** `border-image-source: url()`
- **Slice:** `border-image-slice: 30`
- **Width:** `border-image-width: 10px`
- **Repeat:** `border-image-repeat: stretch | repeat | round`
- **Outset:** `border-image-outset: 5px`
- **Exemplo p1 e p2:** `border-radius: 10px 20px`

## Fontes
- **Onde encontrar:** Google Fonts, Adobe Fonts, Font Squirrel
- **Personalizar fonte:** `font-family: 'NomeDaFonte', sans-serif`
- **@font-face:**  
  ```css
  @font-face {
    font-family: 'MinhaFonte';
    src: url('minhafonte.woff2') format('woff2');
  }
  ```
- **@import url():**
  ```css
  @import url('https://fonts.googleapis.com/css?family=Roboto');
  ```
- **Tamanho:** `font-size: 16px`
- **Estilo:** `font-style: italic | normal`
- **Peso:** `font-weight: bold | 400`
- **Variant:** `font-variant: small-caps`
- **Stretch:** `font-stretch: expanded | condensed`
- **Altura da linha:** `line-height: 1.5`
- **Propriedade resumida:**  
  `font: italic bold 16px/1.5 'Roboto', sans-serif;`

## Sombras
- **Elementos:** `box-shadow: 2px 2px 5px #000`
- **Textos:** `text-shadow: 1px 1px 2px #333`

## Outros
- **Transparência:** `opacity: 0.5`
- **Overflow:** `overflow: hidden | scroll | auto | visible`
- **Redefinir propriedades padrão:**
  ```css
  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }
  ```