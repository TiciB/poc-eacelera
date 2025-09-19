Abaixo está um guia para iniciar o uso de HTTP com Node.js e o módulo HTTP.

Para começar, certifique-se de que o Node.js está instalado em seu sistema. Siga as instruções de instalação no site oficial do [Node.js](https://nodejs.org/pt/download/package-manager).

---

**1. Criando um servidor HTTP simples**

1. Crie um novo arquivo:

    No diretório desejado, crie um arquivo chamado `server.js`.

2. Importe o módulo HTTP:

   Importe o módulo HTTP usando a nova sintaxe:

   ```javascript
   import http from 'http';
   ```

3. Crie o servidor:

   Use o método `createServer` para criar um servidor HTTP:

   ```javascript
    const server = http.createServer((req, res) => {
    res.statusCode = 200;
    res.setHeader('Content-Type', 'text/plain');
    res.end('Hello, World!\n');
    });
   ```

4. Escolha a porta para o servidor escutar:

   Defina a porta e inicie o servidor com o código abaixo:

   ```javascript
   const PORT = 3000;
   server.listen(PORT, () => {
    console.log(`Servidor rodando em http://localhost:${PORT}/`);
   });
   ```

5. Execute o servidor:

   No terminal, navegue até o diretório onde salvou o server.js e execute:

   ```bash
   node server.js
   ```

   Você verá uma mensagem informando que o servidor está em execução.

**2. Testando o servidor**

Abra seu navegador ou uma ferramenta como o Postman e acesse a seguinte URL:

```bash
http://localhost:3000/
```

Você deve ver a mensagem "Hello, World!".

**3. Manipulando rotas**

Você pode expandir seu servidor para responder a diferentes rotas. Veja como:

```javascript
const server = http.createServer((req, res) => {
    if (req.url === '/') {
        res.statusCode = 200;
        res.setHeader('Content-Type', 'text/plain');
        res.end('Página Inicial\n');
    } else if (req.url === '/sobre') {
        res.statusCode = 200;
        res.setHeader('Content-Type', 'text/plain');
        res.end('Página Sobre\n');
    } else {
        res.statusCode = 404;
        res.setHeader('Content-Type', 'text/plain');
        res.end('404 Não Encontrado\n');
    }
});
```

**4. Conclusão**

Neste guia, você aprendeu a criar um servidor HTTP simples usando Node.js com a sintaxe de import, além de manipular rotas. Esse é o primeiro passo para desenvolver aplicações web mais complexas com Node.js.


[Link do vídeo](https://www.youtube.com/watch?v=QnTCre0HHv8&list=PLJ_KhUnlXUPtbtLwaxxUxHqvcNQndmI4B&index=7)

### Referências
[Node.js HTTP Module](https://www.w3schools.com/nodejs/nodejs_http.asp)

