# front-end-ri-happy-2-dio
Ri Happy - Front-end do Zero #2

### Fundamentos do CSS

Os combinadores CSS são operadores (como ` `, >, +, ~) que definem a relação entre dois seletores, permitindo que você estilize elementos com base na sua posição ou hierarquia no documento HTML. Os quatro combinadores principais são o descendente (espaço), que seleciona todos os elementos descendentes; o filho (>), que seleciona apenas filhos diretos; o irmão adjacente (+), que seleciona o irmão imediatamente seguinte; e o irmão geral (~), que seleciona todos os irmãos que seguem o elemento especificado dentro do mesmo pai. 

Tipos de combinadores CSS

1. Combinador Descendente (Espaço)
Símbolo: Um espaço em branco ( ` ` ). 
Função: Seleciona todos os elementos que são descendentes (filhos, netos, bisnetos, etc.) de um elemento especificado. 
Exemplo: div span selecionará todo elemento <span> que está dentro de qualquer elemento <div>, não importa o quão aninhado ele esteja. 
2. Combinador Filho (>)
Símbolo: Maior que (>). 
Função: Seleciona apenas os elementos que são filhos diretos do elemento pai especificado. 
Exemplo: ul > li selecionará todos os elementos <li> que estão diretamente dentro de um elemento <ul>. 
3. Combinador Irmão Adjacente (+)
Símbolo: Mais (+). 
Função: Seleciona um elemento que é o primeiro irmão imediatamente após o elemento especificado anterior, e que compartilham o mesmo pai. 
Exemplo: h1 + p selecionará o primeiro elemento <p> que vem logo após um elemento <h1>. 
4. Combinador Irmão Geral (~)
Símbolo: Tilde (~).

Função: Seleciona todos os elementos que são irmãos do elemento especificado anterior, e que vêm depois dele, desde que todos os elementos compartilhem o mesmo pai. 

Exemplo: h2 ~ p selecionará todos os elementos <p> que seguem um elemento <h2>, contanto que ambos estejam dentro do mesmo elemento pai. 

Por que usar combinadores?

Os combinadores são essenciais para criar regras de estilo mais específicas e eficientes. Eles permitem que você: 

Selecione elementos com base em relacionamentos complexos dentro do DOM (Document Object Model). 
Evite a necessidade de classes adicionais ou identificadores, tornando o código mais limpo e fácil de manter. 
Controle a apresentação de elementos com base na sua posição na estrutura do documento. 
