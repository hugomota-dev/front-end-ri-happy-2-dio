# front-end-ri-happy-2-dio
Ri Happy - Front-end do Zero #2

## Fundamentos CSS

<img width="372" height="305" alt="image" src="https://github.com/user-attachments/assets/77499582-f9ab-4d43-893b-8ede01d0d0ab" />


## 1. O que é CSS?
- **CSS (Cascading Style Sheets)** = Folhas de Estilo em Cascata.  
- Dá **forma e estilo** ao HTML.  
- Com ele é possível:  
  - Definir **cores, fontes e tamanhos**.  
  - Criar **layouts e posicionamentos**.  
  - Deixar o site **responsivo**.  
  - Criar **animações e transições**.  

👉 Analogia: HTML = esqueleto, CSS = roupa, maquiagem e postura.

---

## 2. Forma de declaração
```css
seletor {
  propriedade: valor;
}

/*Exemplo*/

p {
  color: red;
  font-size: 16px;
}
````

### 3. Depuração com DevTools

- Botão direito → Inspecionar (Chrome/Firefox).
- Permite ver e editar CSS em tempo real.

### 4. Seletores (quem vai ser estilizado)

a) Tag
```css
p {
  color: blue;
}
```
Vai afetar todos os <p> do site.
Pouco específico, cuidado pra não virar bagunça.

b) ID (#)
Único por página, mais específico.
```css
#titulo {
  font-size: 32px;
}
```
Analogia: CPF → só existe um igual.

c) Classe (.)
Pode ser usada várias vezes.
```css
.card {
  border: 1px solid black;
}
```
Analogia: time de futebol → vários jogadores (elementos) podem estar na mesma equipe (classe).

d) Universal (*)
```css
* {
  margin: 0;
  padding: 0;
}
```
É o “coringa”, mas gasta desempenho se usado sem critério.

e) Atributo
Seleciona elementos por atributo.
```css
input[type="text"] {
  border: 1px solid gray;
}
```
Útil para diferenciar input text de input password.

f) Combinadores

Os **combinadores CSS** são operadores (` `, `>`, `+`, `~`) que definem a relação entre dois seletores, permitindo estilizar elementos com base na sua posição ou hierarquia no documento HTML. Eles tornam possível aplicar estilos de maneira mais específica, considerando a estrutura do DOM (Document Object Model).

## 5. Tipos de Combinadores CSS

### 5.1. Combinador Descendente (Espaço)
- **Símbolo:** Um espaço em branco ( ` ` )
- **Função:** Seleciona todos os elementos que são descendentes (filhos, netos, bisnetos, etc.) de um elemento especificado.
- **Exemplo:** 
  ```css
  div span {
    /* Seleciona todo <span> que está dentro de um <div>, não importa o quão aninhado */
  }
  ```

---

### 5.2. Combinador Filho (`>`)
- **Símbolo:** Maior que (`>`)
- **Função:** Seleciona apenas os elementos que são filhos diretos do elemento pai especificado.
- **Exemplo:**
  ```css
  ul > li {
    /* Seleciona todos os <li> que estão diretamente dentro de um <ul> */
  }
  ```

---

### 5.3. Combinador Irmão Adjacente (`+`)
- **Símbolo:** Mais (`+`)
- **Função:** Seleciona o elemento que é o primeiro irmão imediatamente após o elemento anterior, compartilhando o mesmo pai.
- **Exemplo:**
  ```css
  h1 + p {
    /* Seleciona o primeiro <p> logo após um <h1> */
  }
  ```

---

### 5.4. Combinador Irmão Geral (`~`)
- **Símbolo:** Tilde (`~`)
- **Função:** Seleciona todos os elementos que são irmãos do elemento especificado e vêm depois dele, desde que compartilhem o mesmo pai.
- **Exemplo:**
  ```css
  h2 ~ p {
    /* Seleciona todos os <p> que seguem um <h2>, dentro do mesmo elemento pai */
  }
  ```
### 5.5. Agrupando seletores
  ```css
h1, h2, p {
  font-family: Arial;
}

  ```
Economiza código, tipo lista de compras: “banana, maçã, laranja → tudo no mesmo saco”.
---

### 5.6. Por que usar combinadores?

Os combinadores são essenciais para criar regras de estilo mais específicas e eficientes. Eles permitem que você:

- Selecione elementos com base em relacionamentos complexos dentro do DOM.
- Evite a necessidade de classes ou identificadores extras, deixando o código mais limpo e fácil de manter.
- Controle a apresentação de elementos considerando sua posição na estrutura do documento.

---

### 6. Tamanhos e dimensões
a) width / height
  ```css
/*Caixa com medida fixa.*/
div {
  width: 200px;
  height: 100px;
}
  ```
b) min-width / min-height

Valor mínimo → não encolhe além disso.
Ex: botão que nunca fica menor que 100px.

c) max-width / max-height

Valor máximo → não cresce mais que isso.
Exemplo: imagens responsivas que não ultrapassam o tamanho do container.

### 7. Tamanhos e dimensões
a) Margin → espaço externo (respiro entre elementos).
  ```css
h1 {
  margin: 20px;
}
  ```
Analogia: espaço do muro pro vizinho.

b) Padding → espaço interno (entre o conteúdo e a borda).
  ```css
button {
  padding: 10px 20px;
}
  ```
Analogia: almofada entre o conteúdo e a caixa.

### 7. Tamanhos e dimensões
Define como o navegador calcula largura/altura.

content-box (padrão): width e height contam só o conteúdo. Padding e border aumentam o tamanho total.

border-box: width e height já incluem conteúdo + padding + borda.
```
* {
  box-sizing: border-box;
}
  ```
