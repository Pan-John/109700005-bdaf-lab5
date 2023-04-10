# 109700005-bdaf-lab5

Here's my token contract address [PeTeCoin](https://goerli.etherscan.io/address/0xd05dE044d4B447607B146d4AC0FA052913465176#writeContract), I accidentally add another `transferOwnership` function cuz i didn't realize that openzeppelin had one. This lab is very interesting although it's quite "expensive" lol, thanks again for the geth Martinet.

### After Deploying the token contact and minting 1000 token:
### 1. Go to [AaveV3 Goerli](https://staging.aave.com/?marketName=proto_goerli_v3) , lend ETH and borrow DAI out.
On the left, Supply 0.05 ETH. On the right, Borrow some DAI (50 or 100)
![2023-4-10下午1 35的影像-1](https://user-images.githubusercontent.com/125814787/230840436-a69c63aa-3545-4e41-8235-2f5cd2d0f8e3.jpg)

### 2. Go to [UniswapV2](https://app.uniswap.org/#/pools/v2) to create a new liquidity pair:
![2023-4-10下午1 35的影像-2](https://user-images.githubusercontent.com/125814787/230840447-b32b8b6b-e0c9-4e45-a378-cbf06473f86c.jpg)

Trying Swap:
![2023-4-10下午1 35的影像-3](https://user-images.githubusercontent.com/125814787/230840454-679db004-0157-4345-8fb5-1c41a3216f99.jpg)

### 3. Create a [Safe (Gnosis’s multiSig solution) on Goerli](https://app.safe.global/new-safe/create)
   - Have 2 owners in the Safe. You can use Metamask to generate the second address.
   - Set the Threshold as 2 out of 2 owners. This means that every time this multiSig is sending a tx, both of these owners have to sign.
![2023-4-10下午1 35的影像-4](https://user-images.githubusercontent.com/125814787/230840456-37f9d2e8-4a95-4653-aa53-b7865f5f9dec.jpg)

### 4. `transferOwnership` of [PeTeCoin](https://goerli.etherscan.io/address/0xd05dE044d4B447607B146d4AC0FA052913465176#writeContract) to the Safe multiSig address. 

### 5. `mint` 10000 of PTC by using Safe multiSig address to your own address 
![2023-4-10下午1 35的影像-5](https://user-images.githubusercontent.com/125814787/230840460-f2e74fe3-396a-48a7-b3fd-cbe1f68b5f48.jpg)

enter token address and abi
![2023-4-10下午1 35的影像-6](https://user-images.githubusercontent.com/125814787/230840462-9afb2484-0c21-4db0-b372-7382cffbe64d.jpg)

enter token address, choose `mint`, enter wallet address and amount.
![2023-4-10下午1 35的影像-7](https://user-images.githubusercontent.com/125814787/230840465-98853d7c-a75a-48ec-9f88-5128111205bb.jpg)
![2023-4-10下午1 35的影像-8](https://user-images.githubusercontent.com/125814787/230840466-6f01e60e-96fd-4444-a151-e5bf85b4fa37.jpg)

### 6. Sign with both owners
It's worth mention that after the last step, the first owner has signed, change the account to the second owner in Metamask and it will pop out another request to sign. Last but not least, remember to execute with the owner that has geth.
![2023-4-10下午1 35的影像-9](https://user-images.githubusercontent.com/125814787/230840473-aaf0ab00-1875-4399-96a9-9a20000e8e6b.jpg)
