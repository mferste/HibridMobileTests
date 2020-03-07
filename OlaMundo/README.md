Olá Mundo

Abaixo segue o aplicativo Express mais simples que você pode criar. É um aplicativo de arquivo único.
Para melhor trabalhar no futuro veremos o gerador Express para um aplicativo completo com vários arquivos JavaScript, modelos Jade e subdiretórios para vários propósitos.

const express = require('express')
const app = express()
const port = 3000
app.get('/', (req, res) => res.send('Hello World!'))
app.listen(port, () => console.log(`Example app listening on port ${port}!`))

Este aplicativo inicia um servidor e escuta na porta 3000 para conexões. O aplicativo responde com "Olá, mundo!" para solicitações ao URL raiz ( /) ou rota . Para todos os outros caminhos, ele responderá com um 404 não encontrado .
O exemplo acima é realmente um servidor que funciona: vá em frente e clique no URL mostrado. Você receberá uma resposta, com registros em tempo real na página, e quaisquer alterações feitas serão refletidas em tempo real. Isso é desenvolvido com o RunKit , que fornece um playground JavaScript interativo conectado a um ambiente completo do Node que é executado no seu navegador da web. Abaixo estão as instruções para executar o mesmo aplicativo em sua máquina local.

Executando localmente
Crie um diretório, mude para ele e execute npm init.
Em seguida, instale express como uma dependência: npm install express --save.
No diretório, crie um arquivo nomeado app.js copie o código abaixo:

    const express = require("express");
    const app = express();
    const port = 3000;
    app.get("/", (req, res) => res.send("Olá mundo!"));
    app.listen(port, () => console.log("Ouvindo na porta " + port));

Lembrando:
O req(pedido) e res(resposta) são exatamente o mesmo objetos que Node fornece, para que possa invocar req.pipe(), req.on('data', callback)e qualquer outra coisa que você faria sem Expresso envolvidos.

Execute o aplicativo com o seguinte comando:
\$ node app.js
Em seguida, carregue http://localhost:3000/em um navegador para ver a saída.
