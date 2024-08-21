# Introdução

## O Que é o NodeJs?

Node.js é uma plataforma de desenvolvimento que permite a execução de código JavaScript fora do navegador, utilizando o motor V8 do Google, que também é usado no Google Chrome. Ele foi criado por Ryan Dahl em 2009 e é amplamente utilizado para construir aplicativos de rede escaláveis e servidores de alto desempenho, principalmente porque permite a construção de aplicações em tempo real e alta capacidade de resposta.

## Sua história

- **Ano de 2009:**
  - Nascimento do Node.js.
  - Criação da primeira versão do npm (Node Package Manager).

- **Ano de 2010:**
  - Desenvolvimento do framework Express (voltado ao desenvolvimento web no Node).
  - Lançamento do Socket.io (framework criado para facilitar a implantação de Sockets).

- **Ano de 2011:**
  - O npm ganha sua versão 1.0.
  - LinkedIn e Uber adotam o Node em seus sistemas.

- **Ano de 2013:**
  - Ghost (primeira grande plataforma de blogs) passa a utilizar o Node.
  - Nascimento da ferramenta web Koa, voltada para o Node.

- **Ano de 2014:**
  - O io.js se torna o maior fork do Node, com o objetivo de introduzir o suporte ao ES6 no mercado.

- **Ano de 2015:**
  - A Node.js Foundation é inaugurada e a quarta versão da ferramenta é lançada.
  - O io.js é incorporado ao Node.

- **Ano de 2017:**
  - O Node ganha sua oitava versão.
  - A V8 introduz o Node.js em sua suíte de testes, tornando a ferramenta oficialmente um mecanismo do JavaScript.

- **Ano de 2020:**
  - O Node.js em sua versão 18 é lançado, incluindo um módulo de test runner nativo, fetch global, melhorias no V8 e novos métodos para arrays.

## Por que utilizar essa ferramenta?

Sem a utilização do Node, a forma de lidar com a concorrência das várias requisições que um sistema recebe seria criando múltiplas threads. Porém, dentro de cada thread criada, há um tempo de resposta que não é aproveitado para nada enquanto a resposta não retorna; como consequência, a CPU fica bloqueada para realizar outras operações.

Com a utilização do Node, diversas requisições podem ser executadas simultaneamente. Em vez de esperar uma resposta para a requisição, ele processa a requisição seguinte da fila. Assim que a resposta da primeira requisição chega, a ferramenta dispara um evento e o callback da requisição (ou seja, a função que executa a resposta) é colocado na fila de requisições e é executado assim que sua vez chegar, finalizando a primeira requisição.

Ele é indicado para uso em:
- APIs
- Aplicações web de chat ou colaborativas para vários usuários
- Jogos multiplayer
- Aplicações que precisam de alta escalabilidade
- Streamings

## Grandes corporações que aderiram ao uso do Node

**Walmart:** No ano de 2013, a empresa migrou todo o seu tráfego mobile para o Node.js durante o período da Black Friday. Foi percebido que seus servidores chegaram a apenas 1% de utilização com 200 milhões de usuários online. [NodeDay](https://dejanglozic.com/2014/03/04/nodeday-2014/)

**PayPal:** Desenvolveu uma aplicação com Node.js e Java, que teve 33% menos linhas de código e 40% menos arquivos, dobrou o número de requisições por segundo e diminuiu em 35% o tempo de resposta. [Medium Paypal](https://medium.com/paypal-tech/node-js-at-paypal-4e2d1d08ce4f)

**Outras empresas que utilizam o Node.js:**
- Netflix
- LinkedIn
- New York Times
- Flickr
- Mozilla
- Yahoo

## Principais Vantagens

**Alta Performance**: Node.js é conhecido por sua alta performance, principalmente em aplicações que exigem grande volume de operações de entrada/saída, como sistemas de chat e servidores de streaming. Isso se deve ao seu modelo de operação baseado em eventos e não-bloqueante, que permite que ele processe múltiplas requisições de forma assíncrona.

**Escalabilidade**: A arquitetura orientada a eventos do Node.js facilita a criação de aplicativos altamente escaláveis. Em vez de criar múltiplas threads, Node.js utiliza um único thread que é capaz de gerenciar milhares de conexões simultaneamente.

**Ecossistema Rico**: O Node.js tem um ecossistema vasto e em constante crescimento, principalmente através do NPM (Node Package Manager), que é o maior repositório de bibliotecas de código aberto. Isso facilita o desenvolvimento, pois muitas funcionalidades já estão disponíveis em pacotes reutilizáveis.

**Comunidade Ativa**: A comunidade do Node.js é grande e ativa, o que significa que há uma vasta quantidade de recursos, tutoriais, e fóruns disponíveis para desenvolvedores. Além disso, a comunidade frequentemente atualiza o Node.js com melhorias e correções de bugs.

**Full-Stack Development**: Com o Node.js, os desenvolvedores podem usar JavaScript tanto no front-end quanto no back-end, o que pode simplificar o desenvolvimento e a manutenção do código, além de reduzir a curva de aprendizado para novos desenvolvedores.

## Principais Desvantagens

**Modelo de Single Thread**: Embora o modelo de single thread do Node.js seja uma vantagem em muitos casos, ele pode se tornar uma desvantagem em aplicações que exigem processamento intensivo de CPU. Em tais situações, o Node.js pode apresentar gargalos de desempenho.

**Inexperiência em Programação Assíncrona**: Desenvolvedores que não estão familiarizados com programação assíncrona podem achar o Node.js desafiador, especialmente quando se trata de lidar com callbacks aninhados, que podem levar ao chamado "callback hell".

**Imaturidade de Algumas Ferramentas**: Embora o ecossistema do Node.js esteja crescendo, algumas bibliotecas e ferramentas ainda estão em fase de desenvolvimento ou são menos maduras em comparação com outras tecnologias, o que pode levar a problemas de estabilidade ou falta de recursos.

**Baixa Compatibilidade com Operações Pesadas de CPU**: Aplicações que envolvem cálculos matemáticos complexos ou outras operações intensivas de CPU podem não ter um bom desempenho no Node.js, uma vez que ele é otimizado para operações de E/S.

## Ferramentas para usar com Node.js

**Express.js**: Um framework minimalista e flexível para Node.js, amplamente utilizado para criar aplicações web e APIs. Ele facilita a criação de servidores e o gerenciamento de rotas.

**Socket.io**: Uma biblioteca que permite a comunicação em tempo real, ideal para aplicações como chats e jogos multiplayer. Ele simplifica a criação de conexões WebSocket.

**NPM (Node Package Manager)**: Ferramenta essencial para gerenciar pacotes e dependências em projetos Node.js. Através do NPM, os desenvolvedores podem instalar e compartilhar bibliotecas e ferramentas.

**PM2**: Um gerenciador de processos para aplicações Node.js. Ele ajuda a monitorar a aplicação em tempo real, reiniciar automaticamente em caso de falhas e gerenciar múltiplas instâncias.

**Mocha**: Um framework de testes para Node.js, que permite a criação de testes unitários e facilita a manutenção e a confiabilidade do código.

**TypeScript**: Embora não seja uma ferramenta exclusiva do Node.js, o TypeScript é amplamente utilizado em projetos Node.js para adicionar tipagem estática ao JavaScript, melhorando a robustez e a escalabilidade do código.

## Sites de Ajuda e Documentação

O site [Node Js Documentation](https://nodejs.org/docs/latest/api/) é a documentação oficial do Node.js, que contém informações detalhadas sobre as APIs e funcionalidades da plataforma.

O site [MDN Web Docs](https://developer.mozilla.org/pt-BR/docs/Learn/Server-side/Express_Nodejs/Introduction) possui tutoriais e guias sobre Node.js e Express.js, que podem ser úteis para desenvolvedores que estão começando a trabalhar com essas tecnologias.