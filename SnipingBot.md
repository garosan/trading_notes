# Sniping Bots 🎯🔫

[EatTheBlocks - 🔴 Crypto Sniping Bot, step-by-step coding tutorial](https://www.youtube.com/watch?v=v7Y7F60YdFQ)

Take a look at [Uniswap Pools](https://app.uniswap.org/explore/pools)

De aquí sacas las address de los contracts de Uniswap V2 [link](https://docs.uniswap.org/contracts/v2/reference/smart-contracts/v2-deployments)

Code:

mkdir sniping-test
cd sniping-test
npm init -y
npm i ethers dotenv

Obtenemos la dirección del factory contract y el ABI.

- [Factory contract code](https://github.com/Uniswap/v2-core/blob/master/contracts/UniswapV2Factory.sol)
- [Factory contract address](https://docs.uniswap.org/contracts/v2/reference/smart-contracts/v2-deployments)
- [ABI Page](https://docs.uniswap.org/contracts/v2/reference/smart-contracts/factory)
- [ABI Json](https://unpkg.com/@uniswap/v2-core@1.0.0/build/IUniswapV2Factory.json)

bot.js

```javascript
const { WebSocketProvider, Contract } = require("ethers");
require("dotenv").config();
const blockchain = require("./blockchain.json");

const provider = new WebSocketProvider(process.env.LOCAL_RPC_URL_WS);
const factory = new Contract(
  blockchain.factoryAddress,
  blockchain.factoryAbi,
  provider
);

const init = () => {
  // setup event listener for new liquidity pool
  factory.on("");
};
```

blockchain.json

```json
  "factoryAddress": "0xF62c03E08ada871A0bEb309762E260a7a6a880E6",
  "factoryAbi": ["Paste abi here"]
```
