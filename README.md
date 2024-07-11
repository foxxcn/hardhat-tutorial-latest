[Power by](https://hardhat.org/tutorial/) @latest



==Tips==

# hardhat



没有自动添加需要手动加入

```sql
npm install --save-dev @nomicfoundation/hardhat-toolbox
将突出显示的行添加到您的中，hardhat.config.js使其看起来像这样：

require("@nomicfoundation/hardhat-toolbox");

/** @type import('hardhat/config').HardhatUserConfig */
module.exports = {
  solidity: "0.8.24",
};
```

set var

```sh
npx hardhat vars set INFURA_API_KEY
✔ Enter value: · ********************************
The configuration variable has been stored in /Users/username/Library/Preferences/hardhat-nodejs/vars.json
```

部署成功

```sh
npx hardhat ignition deploy ./ignition/modules/Token.js --network sepolia
✔ Confirm deploy to network sepolia (11155111)? … yes
Hardhat Ignition 🚀

Deploying [ TokenModule ]

Batch #1
  Executed TokenModule#Token

[ TokenModule ] successfully deployed 🚀

Deployed Addresses

TokenModule#Token - 0x76c95852F6DeAE3A93e42a8950e382826e910AD5
```

etherscan

```sh
npx hardhat vars set ETHERCAN_hardhatMAC
```

开放etherscan验证命令行

```sh
npx hardhat ignition verify chain-11155111
Verifying contract "contracts/Token.sol:Token" for network sepolia...
Successfully verified contract "contracts/Token.sol:Token" for network sepolia:
  - https://sepolia.etherscan.io/address/0x76c95852F6DeAE3A93e42a8950e382826e910AD5#code

```

