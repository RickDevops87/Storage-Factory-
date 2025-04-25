# Storage-Factory-

This repository demonstrates a factory pattern in Solidity using three smart contracts:

1. SimpleStorage.sol – A basic contract that stores and retrieves a number.


2. AddFiveStorage.sol – A child contract that inherits from SimpleStorage and adds custom behavior.


3. StorageFactory.sol – A factory contract that deploys and interacts with instances of SimpleStorage.



Overview

The core contract, StorageFactory, allows for the creation and management of multiple SimpleStorage contracts. Here's a simplified version:

contract StorageFactory {
    SimpleStorage[] public listOfSimpleStorageContracts;

    function createSimpleStorageContract() public {
        // Deploys a new SimpleStorage contract
    }

    function sfStore(uint256 _simpleStorageIndex, uint256 _simpleStorageNumber) public {
        // Stores a number in a specific SimpleStorage instance
    }

    function sfGet(uint256 _simpleStorageIndex) public view returns (uint256) {
        // Retrieves a number from a specific SimpleStorage instance
    }
}

How It Works

1. Deployment – Call createSimpleStorageContract() to deploy a new SimpleStorage contract.


2. Interaction – Use sfStore(index, number) to store a number in a specific deployed contract.


3. Retrieval – Call sfGet(index) to retrieve the stored number.


4. Access Addresses – Access the address of any deployed instance via listOfSimpleStorageContracts(index).



Each SimpleStorage contract is tracked in an array, making it easy to interact with multiple deployed instances.

Summary

This project showcases how a factory contract can dynamically deploy and manage multiple instances of another contract. It provides a simple yet powerful example of modular and scalable smart contract design.
