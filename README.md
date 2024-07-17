<p align="center">
<img
    src="https://example.com/path_to_your_epicchain_logo.png"
    width="125px"
  >
</p>

<h1 align="center">EpicChain</h1>

<p align="center">
    A comprehensive framework for the EpicChain ecosystem written in the Go programming language.
</p>

<p align="center">
  <a href="https://github.com/epicchainlabs/epicchain/releases">
    <img src="https://img.shields.io/github/tag/epicchainlabs/epicchain.svg?style=flat">
  </a>
  <a href="https://circleci.com/gh/epicchainlabs/epicchain/tree/master">
    <img src="https://circleci.com/gh/epicchainlabs/epicchain/tree/master.svg?style=shield">
  </a>
</p>

# Overview
EpicChain is a cutting-edge framework designed to facilitate the development, testing, and deployment of smart contracts on the EpicChain blockchain. The framework leverages the powerful Go programming language, providing developers with a robust set of tools to create efficient and secure smart contracts. Key features include:

- **Golang to EpicChain Virtual Machine (XVM) Bytecode Compiler**: Convert your Go code into bytecode that runs on the EpicChain Virtual Machine.
- **EpicChain Virtual Machine**: Simulate the EpicChain environment to test and debug smart contracts locally.
- **Smart Contract Debugger**: Identify and fix issues in your smart contracts with an integrated debugging tool.
- **Private Network**: Deploy and test smart contracts in a private network before moving to the mainnet.
- **Tooling for Production Deployment**: Seamlessly deploy your smart contracts to production environments.
- **Package Manager**: Manage and reuse smart contract modules written in Go.

# Installation
The following section provides detailed instructions for installing EpicChain and its dependencies.

[**A comprehensive tutorial to get started with EpicChain can be found here**](https://medium.com/@yourtutorial)

## Project Dependencies
### Golang
EpicChain requires a properly installed version of ***Golang***. To install Golang, follow these [installation instructions](https://golang.org/doc/install).

### Godep
For package management, EpicChain uses ***dep***. Install dep by following these [installation instructions](https://github.com/golang/dep).

# Installing the EpicChain Framework
### Unix
EpicChain uses [dep](https://github.com/golang/dep) as its dependency manager. After installing `dep`, run the following command to install EpicChain:
```sh
make install
```

Once the installation is complete, you can find the binary in `bin/epicchain` or use it globally as `epicchain`.

# Getting Started
Explore numerous **example contracts** in the [examples folder](https://github.com/epicchainlabs/epicchain/tree/master/examples) to understand how to build on EpicChain.

### Create a New Smart Contract
To create a new smart contract, run the `init` command:
```sh
epicchain init --name mycontract
```

This command generates a folder named `mycontract` with a `main.go` file in the root directory.

The folder structure will look like this:
```
- mycontract
    - main.go
```

The generated `main.go` file will contain:
```go
package mycontract

import "github.com/epicchainlabs/epicchain/interop/runtime"

func Main(op string, args []interface{}) {
    runtime.Notify("Hello, EpicChain!")
}
```

### Compiling Smart Contracts
To compile a smart contract, use the `compile` command:
```sh
epicchain compile -i path/to/file.go
```
This will output an `.evm` file in the current directory.

You can specify a different output directory using the `-o, --out` flag:
```sh
epicchain compile -i path/to/file.go -o path/to/file.evm
```

# Tutorials
- [Step-by-step guide on issuing your EpicChain token on EpicChain’s Private net using Go](https://medium.com/@yourtutorial)

# Contributing
We welcome contributions from the community! Before contributing, please read our [contributing guidelines](https://github.com/epicchainlabs/epicchain/blob/master/CONTRIBUTING.md).

# Contact
- Join the discussion on the [EpicChain Discord](https://discord.com/invite/u7PmNUpSGg)
- Email us at: support@epic-chain.org

# License
EpicChain is open-source and available under the MIT License.