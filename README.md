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

#### Part 2: Optimize Frames per Second in pizza.html

To optimize views/pizza.html, you will need to modify views/js/main.js until your frames per second rate is 60 fps or higher. You will find instructive comments in main.js. 

You might find the FPS Counter/HUD Display useful in Chrome developer tools described here: [Chrome Dev Tools tips-and-tricks](https://developer.chrome.com/devtools/docs/tips-and-tricks).

### Optimization Tips and Tricks
* [Optimizing Performance](https://developers.google.com/web/fundamentals/performance/ "web performance")
* [Analyzing the Critical Rendering Path](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/analyzing-crp.html "analyzing crp")
* [Optimizing the Critical Rendering Path](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/optimizing-critical-rendering-path.html "optimize the crp!")
* [Avoiding Rendering Blocking CSS](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/render-blocking-css.html "render blocking css")
* [Optimizing JavaScript](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/adding-interactivity-with-javascript.html "javascript")
* [Measuring with Navigation Timing](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/measure-crp.html "nav timing api"). We didn't cover the Navigation Timing API in the first two lessons but it's an incredibly useful tool for automated page profiling. I highly recommend reading.
* <a href="https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/eliminate-downloads.html">The fewer the downloads, the better</a>
* <a href="https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/optimize-encoding-and-transfer.html">Reduce the size of text</a>
* <a href="https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/image-optimization.html">Optimize images</a>
* <a href="https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/http-caching.html">HTTP caching</a>

### Customization with Bootstrap
The portfolio was built on Twitter's <a href="http://getbootstrap.com/">Bootstrap</a> framework. All custom styles are in `dist/css/portfolio.css` in the portfolio repo.

* <a href="http://getbootstrap.com/css/">Bootstrap's CSS Classes</a>
* <a href="http://getbootstrap.com/components/">Bootstrap's Components</a>
