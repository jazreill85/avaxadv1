# ERC20 Token Contract

## Contract Details

### Metadata

- **Name**: Solidity by Example
- **Symbol**: SOLBYEX
- **Decimals**: 18

### State Variables

- `totalSupply`: The total supply of tokens in existence.
- `balanceOf`: A mapping that holds the balance of each account.
- `allowance`: A nested mapping that holds the allowance each account has allowed others to spend on their behalf.

### Events

- `Transfer(address indexed from, address indexed to, uint value)`: Emitted when tokens are transferred from one account to another.
- `Approval(address indexed owner, address indexed spender, uint value)`: Emitted when an account approves another to spend tokens on its behalf.

### Functions

#### `transfer(address recipient, uint amount) external returns (bool)`

Transfers `amount` tokens from the caller's account to `recipient`.

- **Parameters**:
  - `recipient`: The address of the account to transfer tokens to.
  - `amount`: The number of tokens to transfer.
- **Returns**: `true` if the transfer is successful.

#### `approve(address spender, uint amount) external returns (bool)`

Allows `spender` to withdraw from the caller's account multiple times, up to `amount`.

- **Parameters**:
  - `spender`: The address which is approved to spend the tokens.
  - `amount`: The number of tokens `spender` is allowed to spend.
- **Returns**: `true` if the approval is successful.

#### `transferFrom(address sender, address recipient, uint amount) external returns (bool)`

Transfers `amount` tokens from `sender` to `recipient` using the allowance mechanism.

- **Parameters**:
  - `sender`: The address of the account to transfer tokens from.
  - `recipient`: The address of the account to transfer tokens to.
  - `amount`: The number of tokens to transfer.
- **Returns**: `true` if the transfer is successful.

#### `mint(uint amount) external`

Mints `amount` new tokens and assigns them to the caller's account, increasing the total supply.

- **Parameters**:
  - `amount`: The number of tokens to mint.

#### `burn(uint amount) external`

Burns `amount` tokens from the caller's account, decreasing the total supply.

- **Parameters**:
  - `amount`: The number of tokens to burn.

## Usage

1. **Deploy the Contract**: Deploy the contract on an Ethereum network.
2. **Mint Tokens**: Call the `mint` function to create new tokens.
3. **Transfer Tokens**: Use the `transfer` function to send tokens to other accounts.
4. **Approve Spenders**: Allow other accounts to spend tokens on your behalf with the `approve` function.
5. **Transfer From Another Account**: Use the `transferFrom` function to transfer tokens from an approved account.
6. **Burn Tokens**: Destroy tokens you own by calling the `burn` function.

