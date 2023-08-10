# NFT-Identity-Verification

NFTs can be used for identity verification and authentication, as they contain unique information about individual that is Cryptographically secure.

This contract inherits from the OpenZeppelin ERC721
contract and adds identity verification functionality.

The "_verified" mapping keeps track of which addresses have been verified by the contract owner.

The "verify" function allows the contract owner to verify an address, while the 
"revoke function" allows the contract owner to revoke a previously verified address.

The "checkVerifiedOrNot" function allows any address to check if it has been verified by contract owner.

The "mint" function is to allows the contract owner to mint view NFTs and assign them to verified addresses.

The "_beforeTokenTransfer" functoin is to overridden to add the identity verification check.It ensure that both the sender and recipient addresses have been verified before allowing the token transfer to proceed.
