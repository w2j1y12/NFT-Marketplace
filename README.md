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
- Waffle

https://docs.openzeppelin.com/contracts/2.x/api/token/erc721
https://docs.ethers.io/v5/api/contract/contract-factory/
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise

토큰의 수를 추적하는 상태 변수를 선언할 것입니다. 이제 상태 변수는 계약 내에서 선언되지만 해당 계약 내의 모든 함수 외부에 선언된 변수이며 계약 내의 함수만 이러한 상태 변수를 수정할 수 있습니다. 이러한 상태 변수는 블록체인에 저장되며 함수가 상태 변수를 수정할 때마다 블록체인의 상태를 수정하므로 set 함수를 호출하는 데 가스가 발생하므로 일단 코딩하면 이에 대한 보다 구체적인 예를 들겠습니다. 이 nft 계약에 대한 mint 함수를 출력합니다.


```
npx hardhat node
npx hardhat run src/backend/scripts/deploy.js --network localhost
npx hardhat console
- const contract = await ethers getContractAt("NFT", "0x5FbDB2315678afecb367f032d93F642f64180aa3")
- const tokenCount = await contract.tokenCount() -> BigNumber{value:"0"}
- const name = await contract.name() -> 'DApp NFT'
- const symbol = await contract.symbol() -> 'DAPP'
- const marketplace = await ethers.getContractAt("Marketplace","0xDc64a140Aa3E981100a9becA4E685f962f0cF6C9") 
- const feePercent = await marketplace.feePercent() -> BigNumber { value: "1" }
- const feeAccount = await marketplace.feeAccount() -> '0xf39Fd6e51aad88F6F4ce6aB8827279cffFb92266'
- 
```
계약이 배포되면 코드 변경 x -> 따라서 smart contract test는 필수
hardhat framework를 통해 smart contract test 작성 

설정된 가격과 판매자 및 nft가 판매되었는지 여부와 함께 판매된 필드는 부울 유형으로 true 또는 false 값만 보유할 수 있음을 의미합니다.
솔리드의 특수 데이터 구조인 매핑을 사용하여 수행할 수 있습니다. 이것은 키 값 저장소이며 키를 기반으로 항목을 조회할 수 있습니다. 항목 id가 키가 되고 항목 구조가 반환 값이 될 값을 다시 가져옵니다.
