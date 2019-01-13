## Website Performance Optimization portfolio project
### Iniciando

Você já pode começar clonando o repositório:
```
git clone https://github.com/llucasmota/frontend-nanodegree-mobile-portfolio
```
### **Subindo um servidor http no Mac OS / Linux:**
#### Para MacOS/Linux:
* Na pasta do projeto deve-se executar o seguinte comando:
```
cd seu/caminho/
python -m SimpleHTTPServer
```
* Acessando aplicação:
```
localhost:8000/index.html
```
#### Para Windows e demais plataformas:

* Acessando a página principal através da url:
```
seu-caminho/index.html
```
#### Otimizações realizadas no ```index.html```:

* Foi adicionado um atributo media para arquivo css que deve ser carregado apenas para impressão para diminuir o tempo do CRP:
```
  <link href="css/print.css" media="print" rel="stylesheet">
```
* As fontes, antes baixadas diretamente do google fonts, foram adicionadas ao projeto para diminuir o CRP:
```
 <link href="css/font.css" rel="stylesheet">
```
* Adição de atributo ```async``` para scripts ```javascript``` que não são recursos criticos para o carregamento da página:

 ```
  <script src="http://www.google-analytics.com/analytics.js" async></script>
``` 
```
 <script async src="js/perfmatters.js"></script>
```
#### Otimização do ```pizza.html```:
* Foi adicionado atributo ```async```:
```
 <script type="text/javascript" src="js/main.js" async></script>
```
* Otimização de imagens utilizando o aplicativo ImageOptim:
```
https://imageoptim.com/pt-br.html
```
* Ajuste no arquivo ```main.js```:

  * Os métodos retirados ou alteradas tinham repetições desnecessárias e métodos com cálculos de dificil entendimento utilidade:
```
function changePizzaSizes(size) {
    for (var i = 0; i < document.querySelectorAll(".randomPizzaContainer").length; i++) {
      var dx = determineDx(document.querySelectorAll(".randomPizzaContainer")[i], size);
      var newwidth = (document.querySelectorAll(".randomPizzaContainer")[i].offsetWidth + dx) + 'px';
      document.querySelectorAll(".randomPizzaContainer")[i].style.width = newwidth;
```
  * O método novo:
```
var randomPizzas = document.querySelectorAll(".randomPizzaContainer");
    randomPizzas.forEach(function (pizza) {
      pizza.style.width = newWidth + "%";
    });
```
