###### Parte desarrollada en WSL2 -   PROYECTO FAUCET - 
Es un faucet de una red privada de Ethereum
- [X] abrir termianl linux y crear directorio y entrar, de ahi entrar en VS code
- [X] Instalar, a traves de docker(image ETHEREUM CLINET-GO), un nodo Ethereum en local con la networkid xxxx, inicializar y poner en marcha nuestra red privada :
Creamos el nodo Eth, a traves de docker, de nuestra red privada y que tendremos que inicializar con las reglas de la comunidad de euthereum(reglas, pruebas conesnso etc) con el fichero genesis.json,
```bash
docker run -d -p 8545:8545 -p:30303:30303 -v ${PWD}/data:/data -v ${PWD}/genesis.json:/genesis.json --name eth-node ethereum/client-go init --datadir data /genesis.json
```
          
 y ponerla en marcha(la direccion de metamask indicada en el comando es mi direccion de la cuenta 1 de la red de Goerli)
```bash
docker run -d -p 8545:8545 -p 30303:30303 -v ${PWD}/data:/data --name eth-node01 ethereum/client-go --datadir data --http.api personal,eth,net,web3 --http --http.addr 0.0.0.0 --http.port 8545 --mine --miner.etherbase 0xBEb2f649a3A14866D06D41Baaba7Db25b7638B0E --miner.threads=1
```
### en el directorio "geth" se encuentra toda info de la blockchain de ethereum comprobar que haya ido todo bien con
```bash
docker logs <nombre container>
```
y fijarse en que la ChainID se = a la que esta definida en el fichero genesis.json

            ##Conectarse a Metamask 
Para realizar la transferencia creamos una app con nodejs
 
- [X] Configurar esta red en Metamask (crear una nueva red)


###### Parte desarrollada en windows -   PROYECTO FAUCET - 
- [X] Crear directorio y entrar, abrir VS code, yarn init -y   y    yarn.
      Creamos la app (REACT-con 1 solo componente) que llama un file node.js para ejecutar la transaccion de envio de eth
- [ ] Crear un servidor web con node js para firmar la transaccion de envio eth desde la cuenta del faucet a la cuenta conectada con REACT:
      - [ ] creamos directory para ubicar el file index.js y pasamos a VS code, yarn init -y    y   yarn






image.png





