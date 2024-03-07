**BagSubscription Contract**

### Overview
The BagSubscription contract is a Solidity smart contract that facilitates the subscription-based redemption of bags using a custom ERC20 token called BagCoin (BGC). Users can redeem bags of two different types, Safari and Wildcraft, by spending a certain amount of BagCoin tokens. This contract also allows the minting and burning of BagCoin tokens by the contract owner.

### Features
- Subscription-based bag redemption system.
- Two types of bags: Safari and Wildcraft.
- Minting and burning of BagCoin tokens.
- BagCoin token transfer functionality.

### Smart Contract Components
1. **BagSubscription Contract**: The main contract that manages bag redemption and token operations.
2. **ERC20 Token (BagCoin)**: Inherits from OpenZeppelin's ERC20 contract to implement the BagCoin token functionalities.
3. **Ownable**: Inherits from OpenZeppelin's Ownable contract to manage ownership of the contract.

### Functions
- **constructor**: Initializes the BagCoin token with the name "BagCoin" and symbol "BGC" and sets the initial owner.
- **mintTokens**: Allows the contract owner to mint BagCoin tokens and distribute them to specified addresses.
- **burnTokens**: Allows users to burn their BagCoin tokens.
- **redeemBag**: Allows users to redeem bags by spending BagCoin tokens. Users can choose between Safari and Wildcraft bags.
- **transferBagTokens**: Allows users to transfer BagCoin tokens to other addresses.

### Events
- **BagRedeemed**: Fired when a user redeems a bag, indicating the user's address, the type of bag redeemed, and the amount of BagCoin tokens spent.

### Variables
- **userBags**: A mapping that stores the type of bag redeemed by each user.
- **SafariTokenCost**: Constant representing the cost of redeeming a Safari bag in BagCoin tokens.
- **WildcraftTokenCost**: Constant representing the cost of redeeming a Wildcraft bag in BagCoin tokens.

### Usage
1. Deploy the BagSubscription contract, specifying the initial owner address.
2. Mint BagCoin tokens using the `mintTokens` function if necessary.
3. Users can interact with the contract to redeem bags using the `redeemBag` function.
4. Users can transfer BagCoin tokens to other addresses using the `transferBagTokens` function.

### License
This project is licensed under the MIT License. See the SPDX-License-Identifier at the top of the contract file.

