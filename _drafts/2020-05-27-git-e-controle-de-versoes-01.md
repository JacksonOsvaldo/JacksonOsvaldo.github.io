---
layout: post
title: Git e Controle de versões [Parte 01]
excerpt: "Todo desenvolvedor de software mais experiente utiliza Git todos os dias. Desde baixar um arquivo compactado a fazer clone de todo código fonte da versão mais atual de um projeto, essa é uma das ferramentas mais interessantes de se trabalhar com a temática relacionada a controle de versões de um software, gerenciando todos os seus arquivos. Mas, por que falar de Git e de Controle de versões?"
categories: [Desenvolvimento de Software]
comments: true
tag: "Git"
---

Todo desenvolvedor de software mais experiente talvez utilize Git todos os dias. Desde baixar um arquivo compactado a fazer clone de todo código fonte da versão mais atual de um projeto, essa é uma das ferramentas mais interessantes de se trabalhar com a temática relacionada a controle de versões de um software, gerenciando todos os seus arquivos. Mas, por que falar de Git e de Controle de versões?

Recentemente, assisti um [vídeo](https://youtu.be/sx4hAHhO9CY){:target="_blank"} do [Fábio Akita](https://www.instagram.com/akitaonrails/?hl=pt-br){:target="_blank"} onde ele cita um documento, ou uma lista deles, desenvolvido por [Kamran Ahmed](https://github.com/kamranahmedse){:target="_blank"}. Nesse [documento](https://github.com/kamranahmedse/developer-roadmap){:target="_blank"}, o autor elenca todas as principais ferramentas e/ou conhecimentos que, segundo ele, deveriam ser dominados por quem deseje trabalhar como desenvolvedor de software.

Desses documentos, uma das primeiras coisas que Ahmed cita é o Git junto do Controle de Versões (imagem a baixo). Mas, a pergunta vem agora, por quê?

![alt](https://github.com/kamranahmedse/developer-roadmap/raw/master/img/intro.png)

No vídeo, Akita tece toda uma discussão sobre o [assunto](https://youtu.be/sx4hAHhO9CY?t=246){:target="_blank"}. Entretanto, antes de iniciá-la ele faz o seguinte questionamento -- muito interessante, por sinal:

> Como centenas de desenvolvedores podem editar os mesmos códigos em um projeto como o Linux e não virar uma bagunça coloçal?

Akita relaciona isso ao fato da existência de ferramentas como Git. Ou seja, é por conta de todo gerenciamento provido por tecnologias como essa que nós conseguimos tanto controlar, como editar e colocar em produção as mais recentes versões de um determinado software sem que, nesse processo, nos percamos em meio a uma infinidade de códigos, arquivos, diretórios etc.

Então, esse post tem a intenção de explanar um pouco mais o assunto relacionado a Git e a Controle de Versões. Não que faça isso de maneira muito profunda ou avançada demais a ponto de tornar extremamente seleta essa leitura. Pelo contrário. O post será divido em duas partes. A primeira parte, essa aqui, fará uma breve apresentação aos principais conceitos relacionados ao assunto.

Na segunda parte, iremos aplicar esses conceitos em algumas coisas bem práticas e básicas como criar um repositório, fazer um _clone_, um _push_, um _pull_ e por aí vai. E, oh, não se assuste com essas palavras meio estranhas. Vamos aprender juntos o que cada uma delas, pelo menos as principais, significam. Tudo bem?

## O que é controle de versões?

No processo de pensar a escrita desse post me dei conta de uma coisa, eu ainda não sabia o que fundamentava tudo isso. Ou seja, eu não sabia quais eram os fundamentos teóricos de um controle de versões, quem havia pensado, preiramente, nele e quais eram sua reais variações, se existiam.

Então, 

### Quem criou?

Se você fizer uma busca rápida na Wikipédia, verá que a página referente a [Sistemas de Controles de Versão](https://pt.wikipedia.org/wiki/Sistema_de_controle_de_vers%C3%B5es){:target="_blank"} não detém muitos detalhes sobre quem criou ou desenvolveu os conceitos teóricos iniciais sobre o assunto. Porém, ao consultar uma postagem do blog [_The Brewing Press_](http://blog.brew.com.hk/){:target="_blank"} -- obrigado ao Uerlei por ter me ajudado --, conseguimos identificar coisas muito interessantes.

Na postagem, os autores nos levam a entender uma coisa muito interessante. Transcrevendo,

> O controle de versão sempre existiu - ele começou simplesmente com a cópia de toda a base de código em diretórios antigos [traduzido do inglês].

Ou seja, o simples fato de você criar uma pasta no seu computador, organizando o que é, por exemplo, novo, antigo e o que sendo desenvolvido já cumpre o papel desse controle das versões do que você está desenvolvendo. E, com isso, esse processo não ocorre, unicamente, com quem desenvolve software. Ocorre, basicamente, com todo mundo que organiza suas coisas de forma semelhante.



### Como isso funciona?



![alt](https://upload.wikimedia.org/wikipedia/commons/thumb/a/af/Revision_controlled_project_visualization-2010-24-02.svg/220px-Revision_controlled_project_visualization-2010-24-02.svg.png)

### A premissa de antes é a mesma de hoje?

### Git é o Controle de Versões?

## Breve histórico sobre Git

## O que é Git?

<img src="https://git-scm.com/images/progit2.png" width="200" height="300">