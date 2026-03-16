## 🚀 Como executar o projeto

### 1. Iniciar a rede Blockchain

Acesse o diretório da rede de teste do Hyperledger Fabric:

```bash
cd fabric-samples/test-network
```

Derrube qualquer rede que esteja rodando:

```bash
./network.sh down
```

Suba a rede e crie o canal:

```bash
./network.sh up createChannel -c mychannel -ca
```

Faça o deploy do chaincode:

```bash
./network.sh deployCC -ccn basic -ccp ../asset-transfer-basic/chaincode-javascript/ -ccl javascript
```

---

### 2. Configuração da aplicação no VSCode

Abra a pasta do projeto da aplicação:

```bash
hyperledger/fabric-samples/asset-transfer-basic/application-javascript
```

Abra o terminal dentro do VSCode e execute:

```bash
sudo su
npm install
npm install express
node app.js
```
---

### 3. Encerrar a rede Blockchain

Sempre que terminar de utilizar a rede blockchain, execute o comando abaixo dentro da pasta da rede:

```bash
./network.sh down
```

---

### 4. Limpar a carteira da aplicação

No terminal do VSCode, execute:

```bash
rm -rf wallet
```

Esse comando remove os certificados e identidades armazenadas localmente pela aplicação.

---

## 🧰 Tecnologias utilizadas

- Hyperledger Fabric  
- Node.js  
- Express  
- JavaScript  
- Docker
