# Recursos

## Principais Recursos

1. Arquitetura Event Driven e Non Blocking I/O
1. Módulos e NPM (Node Package Manager)
1. Sistema de Eventos
1. Manipulação de Banco de Dados


**Arquitetura Event-Driven e Non-Blocking I/O**

Node.js utiliza um modelo de I/O não-bloqueante e orientado a eventos, o que o torna ideal para aplicações que precisam lidar com um grande número de conexões simultâneas, como servidores web e aplicações em tempo real.

**Exemplo**:

``` javascript
const http = require('http');

const server = http.createServer((req, res) => {
    res.statusCode = 200;
    res.setHeader('Content-Type', 'text/plain');
    res.end('Hello, World!\n');
});

server.listen(3000, '127.0.0.1', () => {
    console.log('Servidor rodando em http://127.0.0.1:3000/');
});

```

**Módulos e NPM (Node Package Manager)**

Node.js segue uma arquitetura modular, permitindo que você use módulos nativos ou de terceiros para adicionar funcionalidades ao seu projeto. O NPM é o gerenciador de pacotes oficial do Node.js, que facilita a instalação, atualização e remoção de pacotes.

**Exemplo**:
``` javascript
// Importando o módulo 'fs' (file system)
const fs = require('fs');

// Lendo um arquivo de forma assíncrona
fs.readFile('arquivo.txt', 'utf8', (err, data) => {
    if (err) throw err;
    console.log(data);
});

``` 

**Sistema de Eventos**

O módulo _events_ permite que você trabalhe com o sistema de eventos do Node.js, que é fundamental para sua arquitetura assíncrona.

**Exemplo**:
``` javascript
const EventEmitter = require('events');

class MeuEmissor extends EventEmitter {}

const meuEmissor = new MeuEmissor();

meuEmissor.on('evento', () => {
    console.log('Um evento ocorreu!');
});

meuEmissor.emit('evento');

``` 

**Manipulação de Banco de Dados**

Node.js pode se conectar a vários tipos de bancos de dados, tanto SQL quanto NoSQL. Abaixo está um exemplo de conexão com o MongoDB usando o Mongoose, um ODM (Object Data Modeling) para MongoDB.

**Exemplo**:
``` javascript
const mongoose = require('mongoose');

mongoose.connect('mongodb://localhost/meubanco', { useNewUrlParser: true, useUnifiedTopology: true });

const db = mongoose.connection;
db.on('error', console.error.bind(console, 'Erro de conexão:'));
db.once('open', function() {
    console.log('Conectado ao MongoDB!');
});

``` 

## Frameworks Populares

**Express.js**

Express.js é um framework web minimalista e flexível para Node.js, que fornece uma série de recursos para criar aplicações web e APIs de forma rápida e eficiente.

* **Exemplo**:
``` javascript
const express = require('express');
const app = express();

app.get('/', (req, res) => {
    res.send('Hello, World!');
});

app.listen(3000, () => {
    console.log('Servidor Express rodando na porta 3000');
});
```	

* **Socket.io**

Socket.io é uma biblioteca que permite comunicação em tempo real entre clientes e servidores.

* **Exemplo**:

``` javascript
const io = require('socket.io')(3000);

io.on('connection', socket => {
    console.log('Novo cliente conectado');
    socket.emit('message', 'Bem-vindo!');
    
    socket.on('message', msg => {
        console.log('Mensagem recebida: ' + msg);
    });
});

```	

**Streaming de Dados**

Node.js é ideal para o processamento de streams de dados, como arquivos de áudio e vídeo.

**Exemplo**:

``` javascript
const fs = require('fs');

const readStream = fs.createReadStream('arquivo_grande.txt', 'utf8');
const writeStream = fs.createWriteStream('saida.txt');

readStream.pipe(writeStream);

readStream.on('data', chunk => {
    console.log('Novo pedaço recebido:', chunk);
});
``` 
## Módulos Node.js
O Node.js possui várias ferramentas que podem ajudar no desenvolvimento web do lado do servidor. Abaixo temos alguns exemplos:


| **Ferramenta**      | Usada para    |
| :---------- | :-------------- |
| `gm, sharp`       | Manipulação de imagem, incluindo edição, redimensionamento, compactação e assim por diante, diretamente no seu código JavaScript  |
| `PDFKit`       | Geração de PDF |
| `validator.js`    | Validação de cadeia de caracteres |
| `imagemin, UglifyJS2`       | Minificação |
| `spritesmith`    | Geração de folha de Sprite |
| `winston`    | Registro em log |
| `commander.js`    | 	Criação de aplicativos de linha de comando |

!!! tip
    Você pode usar o módulo do sistema operacional Node.js para realizar ações como verificar a plataforma e retornar uma variável específica da plataforma: Win32/.bat para desenvolvimento do Windows, Darwin/.sh para Mac/unix, Linux, SunOS e assim por diante (por exemplo, `var isWin = process.platform === "win32";`).

### Outros Sites para Aprender Node.js

[Link para o site oficial do node](https://nodejs.org/pt)

[Link para o site da mozilla](https://developer.mozilla.org/pt-BR/docs/Glossary/Node.js)

[Link para a documentação do Node na W3Schools](https://www.w3schools.com/nodejs/nodejs_intro.asp)
