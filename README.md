# PSEUDO-ELEMENTOS
Hoje vamos revisar os pseudo-elementos em CSS.

O que são pseudo-elementos?
Pseudo-elementos são palavras-chave adicionadas a seletores em CSS que permitem estilizar partes específicas de um elemento sem precisar adicionar classes extras no HTML.

Sintaxe básica:

```
seletor::pseudo-elemento {
  propriedade: valor;
}
```

Em CSS3 usamos :: (dois pontos) para indicar pseudo-elementos, embora : ainda funcione para compatibilidade com versões antigas.
:
Pseudo-elementos mais usados:

1.   ::before e ::after
Permitem adicionar conteúdo antes ou depois do conteúdo de um elemento, via CSS.

Exemplo prático:

```
<h2 class="titulo">Olá, mundo!</h2>
```

```
.titulo::before {
  content: "🌟 ";
  color: gold;
}

.titulo::after {
  content: " 🚀";
  color: red;
}
```
Dica: Use ::before e ::after para adicionar ícones, efeitos visuais, aspas, ou decorações sem alterar o HTML.

2.   ::first-line
Aplica estilos apenas à primeira linham de um texto.

```
<p class="descricao">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum a vehicula metus.</p>
```

```
.descricao::first-line {
  font-weight: bold;
  color: #2c3e50;
}
```
Ideal para destacar introduções ou dar um toque de estilo à primeira linha de parágrafos em artigos e blogs.

3.   ::first-letter

```
.descricao::first-letter {
  font-size: 2em;
  color: #e74c3c;
  float: left;
  padding-right: 5px;
}
```
Pode ser usado para fazer aqueles efeitos de letra capitular, muito usado em livros e revistas.

4.  ::selection
Permite estilizar a parte do texto selecionada pelo usuário (quando ele arrasta com o mouse).

```
::selection {
  background: #ffcb05;
  color: #000;
}
```
Excelente para dar identidade à sua marca, até quando o usuário seleciona o texto!

Use pseudo-elementos quando...
Decoração | Quer adicionar conteúdo visual sem alterar o HTML
Design editorial | Quer destacar a primeira linha/letra
Efeitos | Precisa de detalhes visuais que mudam com hover, foco, etc.
Acessibilidade | Deseja evitar poluir o HTML com ícones puramente visuais

Combinações úteis
Adicionar ícones com Font Awesome ou Unicode:

```
.botao::before {
  content: "\2713"; /* checkmark unicode */
  margin-right: 8px;
}
```
