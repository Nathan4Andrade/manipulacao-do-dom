# manipulacao-do-dom

## O que é DOM?

DOM (acrônimo de Document Object Model) é uma representação estruturada em forma de árvore de um documento HTML ou XML. Ele fornece uma interface programática para manipular o conteúdo e a estrutura do documento, permitindo que os desenvolvedores criem dinamicamente e alterem o conteúdo de uma página da web usando JavaScript ou outras linguagens de script.
O DOM é dividido em nós que representam diferentes partes do documento, como elementos HTML, atributos, texto e comentários. Cada nó pode ter filhos, irmãos e um pai, formando assim uma árvore hierárquica.
O uso do DOM é fundamental para a criação de sites interativos e dinâmicos, permitindo a manipulação do conteúdo e da aparência da página em tempo real, sem precisar recarregar a página. Além disso, ele também é usado em outras tecnologias web, como CSS e XML.

~~~html
<!DOCTYPE html>
<html>
  <head>
    <title>Exemplo DOM</title>
  </head>
  <body>
    <h1 id="titulo">Olá mundo!</h1>
    <p>Este é um exemplo de uso do DOM.</p>
    <script src="script.js"></script>
  </body>
</html>
~~~

~~~javascript
// seleciona o elemento <h1> pelo seu ID
var titulo = document.getElementById("titulo");

// muda o conteúdo do elemento
titulo.innerHTML = "Novo título";

// adiciona uma nova classe CSS ao elemento
titulo.classList.add("destaque");

// seleciona todos os elementos <p> na página
var paragrafos = document.getElementsByTagName("p");

// altera o conteúdo de todos os parágrafos
for (var i = 0; i < paragrafos.length; i++) {
  paragrafos[i].innerHTML = "Este texto foi alterado pelo JavaScript.";
}
~~~
#
## O que são os objetos window e document?

`window` e `document` são objetos nativos do JavaScript que são fundamentais para a interação com o DOM e a manipulação de páginas web.

O objeto window representa a janela do navegador e fornece uma interface para interagir com ela. Ele é a raiz do objeto global em um navegador e contém muitas propriedades e métodos úteis para trabalhar com a janela do navegador, incluindo redimensionamento, movimento, manipulação de cookies, gerenciamento de histórico de navegação, entre outras.

Já o objeto document representa a página carregada em uma janela do navegador e fornece uma interface para interagir com o conteúdo da página. Ele é um objeto filho do objeto window e contém muitas propriedades e métodos úteis para trabalhar com o DOM, como acesso a elementos HTML, criação e exclusão de elementos, alteração de conteúdo, manipulação de formulários, entre outras.

Em resumo, o objeto window é responsável pela manipulação da janela do navegador, enquanto o objeto document é responsável pela manipulação do conteúdo da página. Ambos são objetos fundamentais no desenvolvimento de páginas web dinâmicas e interativas.

~~~javascript
// define uma variável global usando o objeto window
window.nome = "João";

// adiciona um novo elemento ao documento usando o objeto document
var paragrafo = document.createElement("p");
paragrafo.textContent = "Bem-vindo, " + nome + "!";
document.body.appendChild(paragrafo);

// abre uma nova janela usando o objeto window
var novaJanela = window.open("http://www.exemplo.com", "janelaExemplo", "width=600,height=400");

// define um temporizador para fechar a janela após 5 segundos
setTimeout(function() {
  novaJanela.close();
}, 5000);
~~~
