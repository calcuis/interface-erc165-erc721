# interface ERC165-721

The Solidity code describes a standard implementation for `ERC721` Non-Fungible Tokens, including interfaces for receiving and checking `ERC721` token support, and a base contract that provides standard token management functions.

The smart contract allows developers to create their own unique, non-fungible tokens (unique and cannot be replicated).

The contract defines several interfaces and an abstract contract that the `ERC721` token contract extends. The IERC721Receiver interface defines a function that a contract must implement to receive `ERC721` tokens. The `IERC165` interface specifies a function for checking whether a contract supports a particular interface.

The `ERC165` abstract contract implements the IERC165 interface and provides a default implementation of the supportsInterface function. The `IERC721` interface defines functions for transferring tokens, querying token ownership, and managing approvals. The `IERC721Metadata` interface extends the `IERC721` interface and adds functions for querying the name, symbol, and token URI of the token.

The `ERC721` contract is the main implementation of the `ERC721` token contract. It extends the `Context`, `ERC165`, `IERC721`, and `IERC721Metadata` interfaces. It defines storage variables for the name, symbol, ownership information, and approval information of the tokens. The contract implements functions for querying balances, token ownership, and metadata, as well as functions for transferring, approving, and minting tokens.

The contract also implements an internal function for transferring tokens, a function for checking whether a caller is authorized to transfer a token, and a function for safely transferring tokens. The `_safeTransfer` function transfers a token and checks whether the recipient has implemented the `onERC721Received` function to receive the token. The contract also defines a function for setting the base URI for token metadata.


### References

https://github.com/OpenZeppelin/openzeppelin-contracts/blob/master/contracts/token/ERC721/IERC721Receiver.sol
https://github.com/OpenZeppelin/openzeppelin-contracts/blob/master/contracts/utils/introspection/IERC165.sol
https://github.com/OpenZeppelin/openzeppelin-contracts/blob/master/contracts/utils/introspection/ERC165.sol
https://github.com/OpenZeppelin/openzeppelin-contracts/blob/master/contracts/token/ERC721/IERC721.sol
https://github.com/OpenZeppelin/openzeppelin-contracts/blob/master/contracts/token/ERC721/extensions/IERC721Metadata.sol
https://github.com/OpenZeppelin/openzeppelin-contracts/blob/master/contracts/token/ERC721/ERC721.sol
