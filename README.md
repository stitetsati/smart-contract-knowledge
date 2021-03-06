# Smart Contract Related Blog Posts

## Solidity
- [Virtual vs Override](https://medium.com/upstate-interactive/solidity-override-vs-virtual-functions-c0a5dfb83aaf)
    1. virtual: allow inheriting contract to override
    2. override: mark a function as overriding some parent function
    3. override is required even if the function is implementing an interface
- [Storage](https://medium.com/coinmonks/how-to-read-private-variables-in-contract-storage-with-truffle-ethernaut-lvl-8-walkthrough-b2382741da9f)
    1. Variables are stored in 32-byte slots, in sequence of their declarations
    2. Private variables are still accessible with `web3.eth.getStorageAt(contractAddress, slotNumber)`
- [view vs pure functions](https://docs.soliditylang.org/en/develop/contracts.html#view-functions)
    1. view does not modify states
    2. pure does not modify states AND does not read states
- Casting a Bytes32 to Bytes16
    1. Just take 16 bytes from left to right (from most significant bit) <WRONG>
    2. Just take 16 bytes from right to left (from least significant bit)(https://medium.com/coinmonks/ethernaut-lvl-13-gatekeeper-1-walkthrough-how-to-calculate-smart-contract-gas-consumption-and-eb4b042d3009)

- Revert without reason
    1. Has the request reach the destination address? Check some view functions, read some storage data.
    2. If reachable, then must be function param / calldata error. Can either read through code line by line or test other param combination.
