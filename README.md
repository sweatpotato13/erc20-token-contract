# ERC20-token-contract

## Prerequisite
```
npm install -g truffle
```

## Usage

### 1. Install dependency
```bash
yarn install
```

### 2. Change TokenName, TokenSymbol, Initial Supply
```ts
// contracts/Token.sol
contract Token is ERC20, ERC20Burnable, ERC20Snapshot, Ownable, Pausable, ERC20Permit {
    constructor() ERC20("TokenName", "TokenSymbol") ERC20Permit("TokenName") {
        _mint(msg.sender, ${InitialSupply} * 10 ** decimals());
    }
```
### 3. Make .infuraKey, .secret files
```text
infuraKey : infura project id
secret : mnemonic of wallet
```

### 4. run truffle
```bash
# for local
yarn start:dev
# for ropsten testnet
yarn start:testnet
```

### 5. (Optional) Check etherscan.io
if you deploy contract to ropsten or other testnet, then you can check from etherscan.io