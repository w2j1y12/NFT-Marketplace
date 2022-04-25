# NFT-Marketplace

### Youtube : https://www.youtube.com/watch?v=2bjVWclBD_s
### Github : https://github.com/dappuniversity/nft_marketplace

```
npm install -- save-dev hardhat@2.8.4
git clone https://github.com/dappuniversity/starter_kit_2.git NFT-Marketplace
npm install react-router-dom@6
npm install ipfs-http-client@56.0.1
npm i @openzepplin/contracts@4.5.0
```

- nodejs
- hardhat
- metamask
- OpenZeppelin

https://docs.openzeppelin.com/contracts/2.x/api/token/erc721
https://docs.ethers.io/v5/api/contract/contract-factory/
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise

토큰의 수를 추적하는 상태 변수를 선언할 것입니다. 이제 상태 변수는 계약 내에서 선언되지만 해당 계약 내의 모든 함수 외부에 선언된 변수이며 계약 내의 함수만 이러한 상태 변수를 수정할 수 있습니다. 이러한 상태 변수는 블록체인에 저장되며 함수가 상태 변수를 수정할 때마다 블록체인의 상태를 수정하므로 set 함수를 호출하는 데 가스가 발생하므로 일단 코딩하면 이에 대한 보다 구체적인 예를 들겠습니다. 이 nft 계약에 대한 mint 함수를 출력합니다.


```
npx hardhat node
```
