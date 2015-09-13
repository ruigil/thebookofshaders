# Introdução

<canvas id="custom" class="canvas" data-fragment-url="cmyk-halftone.frag" data-textures="vangogh.jpg" width="700px" height="320px"></canvas>

As imagens acima foram feitas de forma differente. A primeira foi feita pela mão de Van Gogh, que aplicou camada en cima de camada de tinta. Demorou-lhe horas. A segunda foi produzida em segundos pela combinação de quatro matrizes de pixels: uma para a cor ciano, uma para magenta, uma para amarelo e uma para preto. A diferença principal é que a segunda imagem foi produzida de uma forma não-sequencial (o que quer dizer que não foi passo a passo, mas tudo ao mesmo tempo).

Este livro é sobre a técnica computacional revolucionária, *fragment shaders*, que está a levar as imagens geradas digitalmente ao próximo nível. Podes compará-la ao equivalente da prensa de Gutenberg para os gráficos.

![Gutenberg's press](gutenpress.jpg)

Os shaders de fragmentos dão-te controlo total sobre os pixeis que são apresentados no ecrã a velocidades super rápidas. É por isso que eles são usados em todo o tipo de casos, desde filtros de vídeo nos télémoveis até jogos de vídeo 3D incríveis.

![Journey by That Game Company](journey.jpg)

Nos capítulos seguintes irás descobrir como incrivelmente rápida e poderosa é esta técnica, e como aplicá-la ao teu trabalho pessoal e profissional.

## Para quem é este livro?

Este livro é escrito para programadores criativos, desenvolvedores de jogos e engenheiros que tenham experiência de programação, um conhecimento básico de algebra linear e trigonometria, e que queiram levar o seu trabalho a um excitante novo nível de qualidade gráfica. (Se queres aprender a programar, eu recomendo que comeces com [Processing](https://processing.org/) e que voltes mais tarde quando já estiveres confortável com a programação.)

Este livros vai ensinar-te como podes usar e integrar shaders nos teus projetos, melhorando a sua performance e qualidade gráfica. Os shaders GLSL (OpenGL Shading Language) compilam e correm numa variedade de plataformas, por isso serás capaz de aplicar o que aprenderás aqui em qualquer ambiente que usa OpenGL, OpenGL ES ou WebGL. Por outras palavras, serás capaz de aplicar e utilizar o teu conhecimento com os esboços [Processing](https://processing.org/), aplicações [openFrameworks](http://openframeworks.cc/), instalações interactivas com [Cinder](http://libcinder.org/), websites ou jogos iOS/Android com [Three.js](http://threejs.org/).

## O que é que este livro cobre?

Este livro irá focalizar-se no uso de pixel shaders GLSL. Primeiro iremos definir o que são os shaders; depois iremos aprender como fazer formas procedimentais, padrões, texturas e animações com eles. Irás aprender os fundamentos da linguagem de shading e depois aplicá-la a cenários mais úteis como: processamento de imagem (operações de imagens, matrizes de convolução, desfocagem, filtros de cor, tabelas de indices e outros efeitos) e simulações (o jogo da vida de Conway, a reação-difusão de Gray-Scott, ondas de água, efeitos de pintura de água, células de Voronoi, etc.). Para o final do livro iremos ver um conjunto de técnicas avançadas baseadas em Ray Marching.

*Existem exemplos interactivos em cada capítulo para tu poderes brincar.* Quando mudares o código, irás ver as mudanças imediatamente. Os conceitos podem ser abstractos e confusos, por isso os exemplos interactivos são essenciais para te ajudar a aprender o material. Quando mais rápido puseres os conceitos em prática, mais facil irá ser o processo de aprendizagem.

O que este livro não cobre:

* Este *não é* um livro sobre OpenGL ou WebGL. O OpenGL/WebGL é um assunto maior do que o GLSL ou os pixel shaders. Para aprenderes mais sobre OpenGL/WebGL eu recomendo que dês uma vista de olhos a: [OpenGL Introduction](https://open.gl/introduction), [the 8th edition of the OpenGL Programming Guide](http://www.amazon.com/OpenGL-Programming-Guide-Official-Learning/dp/0321773039/ref=sr_1_1?s=books&ie=UTF8&qid=1424007417&sr=1-1&keywords=open+gl+programming+guide) (também conhecido como o livro vermelho) ou [WebGL: Up and Running](http://www.amazon.com/WebGL-Up-Running-Tony-Parisi/dp/144932357X/ref=sr_1_4?s=books&ie=UTF8&qid=1425147254&sr=1-4&keywords=webgl)

* Este *não é* um livro de matemática. Apesar de irmos cobrir um conjunto de algoritmos e técnicas que dependem de um conhecimento de algebra e trigonometria, nós não iremos explicá-las em detalhe. Para questões relacionadas com a matemática, eu recomendo ter uma destes livros por perto: [3rd Edition of Mathematics for 3D Game Programming and computer Graphics](http://www.amazon.com/Mathematics-Programming-Computer-Graphics-Third/dp/1435458869/ref=sr_1_1?ie=UTF8&qid=1424007839&sr=8-1&keywords=mathematics+for+games) ou [2nd Edition of Essential Mathematics for Games and Interactive Applications](http://www.amazon.com/Essential-Mathematics-Games-Interactive-Applications/dp/0123742978/ref=sr_1_1?ie=UTF8&qid=1424007889&sr=8-1&keywords=essentials+mathematics+for+developers).

## O que é que precisas para começar?

Não muito! Se tens um browser moderno que pode executar WebGL (como o Chrome, Firefox ou Safari) e uma ligação internet, clica no botão "Próximo" capítulo  no fim desta página para começar.

Not much! If you have a modern browser that can do WebGL (like Chrome, Firefox or Safari) and a internet connection, click the “Next” Chapter button at the end of this page to get started.

Em alternativa, baseado no que tens, ou no que precisas deste livro podes:

- [Criar uma versão off-line deste livro](http://thebookofshaders.com/appendix/)

- [Executar os exemplos num RaspberryPi sem um browser](http://thebookofshaders.com/appendix/)

- [Criar um PDF deste livro para imprimir](http://thebookofshaders.com/appendix/)

- Usar o [repositório on-line](https://github.com/patriciogonzalezvivo/thebookofshaders) para ajudar a resolver problemas e partilhar código.
