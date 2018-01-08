# Overview

This is a curated collection of resources on secialized programming languages executed by decentralized peer-to-peer networks, also known as blockchains.

Let us define a smart contract, or simply contract, as a piece of code created by a blockchain user and executed by a blockchain node. A smart contract language (SCL) is a programming language that is either used to write a smart contract directly, or is compiled to it.

Programming languages differ on multiple dimensions, such as [paradigm](https://en.wikipedia.org/wiki/Programming_paradigm) and [type system](https://en.wikipedia.org/wiki/Type_system). Due to a very unusual execution environment, SCLs have a different set of trade-offs compared to earlier languages. This spawned multiple attempts at creating secure and expressive SCLs.

# Pre-Bitcoin

* [A formal language for analyzing contracts](http://nakamotoinstitute.org/contract-language/) - an essay by Nick Szabo

# Bitcoin

* [Bitcoin Script](https://en.bitcoin.it/wiki/Script) - a stack-based non Turing complete Forth-like language used to write script that determine whether a UTXO can be spent.
* [Ivy](https://github.com/ivy-lang/ivy-bitcoin) - a non Turing complete higher-level language that compiles to Bitcoin Script ([announcement](https://blog.chain.com/ivy-for-bitcoin-a-smart-contract-language-that-compiles-to-bitcoin-script-bec06377141a))
* [Simplicity](https://blockstream.com/2017/10/30/simplicity.html) - a typed functional programming language utilizing combinators [blog post](https://medium.com/@danrobinson/understanding-simplicity-implementing-a-smart-contract-language-in-30-lines-of-haskell-827521bfeb4d), [another one](https://iohk.io/blog/simplicity-and-michelson/)
* [Rootstock](https://www.rsk.co/) - do they use their own language?


# Ethereum

* Ethereum bytecode - a Turing complete stack-based languge executed by the Ethereum virtual machine (EVM)
* [Solidity](https://solidity.readthedocs.io/en/develop/) - a high-level imperative statically typed language compiled to EVM ([docs](https://solidity.readthedocs.io/en/develop/))
* LLL - a "low-level Lisp-like language" compiled to EVM bytecode ([blog post](https://media.consensys.net/an-introduction-to-lll-for-ethereum-smart-contract-development-e26e38ea6c23), [series of blog posts](http://blog.syrinx.net/))
* [Viper](https://github.com/ethereum/vyper) - a high-level language compiled to EVM ([announcement of formal tools from RV](https://runtimeverification.com/blog/?p=617))
* [Bamboo](https://github.com/pirapira/bamboo) - a high-level "formal-verification-friendly" language compiled to EVM
* [functional-solidity-language](https://github.com/raineorshine/functional-solidity-language) - pretty much self-descriptive :)
* [eWASM](https://github.com/ewasm) - a restricted subset of [WebAssembly](http://webassembly.org/) for Ethereum contracts
* Serpent - a Python-like high-level language compiled to EVM (deprecated due to [security issues with the compiler](https://blog.zeppelin.solutions/serpent-compiler-audit-3095d1257929))
* Mutan - a C-like language compiled to EVM (deprecated)
* [Idris](https://www.idris-lang.org/) - a pure functional language with dependent types; [Pettersson and Edström](https://publications.lib.chalmers.se/records/fulltext/234939/234939.pdf) used it to write contracts that compile to EVM via Serpent
* [JULIA](https://solidity.readthedocs.io/en/develop/julia.html) (IULIA?) - an intermediate low-level language ([blog post](https://medium.com/@chriseth/writing-smart-contracts-in-iulia-2a5ba737c7f1))
* [Babbage](https://medium.com/@chriseth/babbage-a-mechanical-smart-contract-language-5c8329ec5a0e) - "a mechanical smart contract language"
* [Pyramid](https://github.com/MichaelBurge/pyramid-scheme) - An EVM backend for SICP Scheme


## DSLs

* [Findel](https://github.com/cryptolu/findel) - a non Turing complete financial DSL inspired by a [S.P.Jones' work](https://www.microsoft.com/en-us/research/publication/composing-contracts-an-adventure-in-financial-engineering/)
* the language from [the paper](https://link.springer.com/article/10.1007/s12599-017-0507-z) by Egelund-Müller et al


# Other blockchains

* [Michelson](http://www.michelson-lang.com/) - a stack based and strongly typed domain-specific language (Tezos)
* [Liquidity](http://www.liquidity-lang.org/) - a high-level typed smart-contract language that strictly complies to Michelson security restrictions (Tezos)
* [Plutus](https://github.com/input-output-hk/plutus-prototype) - a pure functional language with user-defined data types and polymorphism (Cardano)
* [Rholang](https://rholang.rchain.coop/) - a reflective higher-order process calculus language (RChain)
* [Obsidian](https://mcoblenz.github.io/Obsidian/) - a state-oriented language with linear types
* [DAML](http://hub.digitalasset.com/blog/introducing-the-digital-asset-modeling-language-a-powerful-alternative-to-smart-contracts-for-financial-institutions)

# Other links

* https://github.com/pirapira/fp-ethereum - a collection of links related to function programming for Ethereum
* [Smart Contract Languages Development to Follow](https://blog.comae.io/smart-contract-languages-development-to-follow-992e30774b39) - a post by Matt Suiche, Comae (Dec 2017)
