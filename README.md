# Overview

This is a curated collection of resources on specialized programming languages executed by decentralized peer-to-peer networks, also known as blockchains.

Let us define a smart contract, or simply contract, as a piece of code created by a blockchain user and executed by a blockchain node. A smart contract language (SCL) is a programming language that is either used to write a smart contract directly, or is compiled to it.

Programming languages differ on multiple dimensions, such as [paradigm](https://en.wikipedia.org/wiki/Programming_paradigm) and [type system](https://en.wikipedia.org/wiki/Type_system). Due to a very unusual execution environment, SCLs have a different set of trade-offs compared to earlier languages. This spawned multiple attempts at creating secure and expressive SCLs.

# Pre-Bitcoin

* [A formal language for analyzing contracts](http://nakamotoinstitute.org/contract-language/) - an essay by Nick Szabo
* [E](http://www.erights.org/) - referenced by Szabo

# Bitcoin

* [Bitcoin Script](https://en.bitcoin.it/wiki/Script) - a stack-based non Turing complete Forth-like language used to write script that determine whether a UTXO can be spent.
* [Ivy](https://github.com/ivy-lang/ivy-bitcoin) - a non Turing complete higher-level language that compiles to Bitcoin Script ([announcement](https://blog.chain.com/ivy-for-bitcoin-a-smart-contract-language-that-compiles-to-bitcoin-script-bec06377141a))
* [Simplicity](https://github.com/ElementsProject/simplicity) - a typed functional programming language utilizing combinators [blog post](https://medium.com/@danrobinson/understanding-simplicity-implementing-a-smart-contract-language-in-30-lines-of-haskell-827521bfeb4d), [another one](https://iohk.io/blog/simplicity-and-michelson/)
* [BitML](https://github.com/bitml-lang/bitml-compiler) - a process calculus based language, compiles to Bitcoin script ([article](https://eprint.iacr.org/2018/122))
* [BALZaC](https://blockchain.unica.it/balzac/docs/) - a high-level language based on the formal model proposed in [[AB+18FC]](https://eprint.iacr.org/2017/1124.pdf)
* [Miniscript](http://bitcoin.sipa.be/miniscript/) - a language for writing (a subset of) Bitcoin Scripts in a structured way, enabling analysis, composition, generic signing and more
    * [Policy Language](http://diyhpl.us/wiki/transcripts/stanford-blockchain-conference/2019/miniscript/) - nicer language that compiles to Miniscript
* [Sapio](https://www.coindesk.com/this-new-coding-language-could-help-unlock-bitcoins-smart-contract-potential)
* [Minsc](https://min.sc/) - a high-level scripting language for expressing Bitcoin Script spending conditions based on Miniscript Policy


# Ethereum

Active:
* [Ethereum bytecode](https://ethervm.io/) - a Turing complete stack-based language executed by the Ethereum virtual machine (EVM)
* [Solidity](https://github.com/ethereum/solidity) - a high-level imperative statically typed language compiled to EVM. [Docs](https://solidity.readthedocs.io/en/latest/)
* [Vyper](https://github.com/vyperlang/vyper) - a high-level language compiled to EVM ([announcement of formal tools from RV](https://runtimeverification.com/blog/?p=617)). [Docs](https://vyper.readthedocs.io/en/latest/)
* [Fe](https://github.com/ethereum/fe) - a language inspired by Vyper aiming to achieve its goals. [Docs](https://fe.ethereum.org/docs/index.html)
* [eWASM](https://github.com/ewasm/design) - a restricted subset of [WebAssembly](http://webassembly.org/) for Ethereum contracts. [Docs](https://ewasm.readthedocs.io/en/mkdocs/)
* [Idris](https://github.com/idris-lang/Idris2) - a pure functional language with dependent types. [Docs](http://docs.idris-lang.org/en/latest/)
* [Flint](https://github.com/flintlang/flint) - a type-safe, contract-oriented programming language specifically designed for writing robust smart contracts on Ethereum
* [Formality](https://github.com/MaiaVictor/Formality) - an efficient programming language featuring formal proofs
* [Huff](https://github.com/AztecProtocol/huff) - an efficient low-level language with macros
* [Lira](https://github.com/etoroxlabs/lira) - a declarative domain-specific language for defining simple yet highly complex financial contracts for EVM
* [Zinc](https://github.com/matter-labs/zinc) - a language to write zero-knowledge circuits and ZKP-based smart contracts. [Docs](https://zinc.zksync.io/)
* [Sway](https://www.youtube.com/watch?v=S52ZsZ7rNOo) - a Rust-based Smart Contract Language

No updates after 2018:
* [Bamboo](https://github.com/pirapira/bamboo) - a high-level "formal-verification-friendly" language compiled to EVM
* [Pyramid](https://github.com/MichaelBurge/pyramid-scheme) - An EVM backend for SICP Scheme
* [Lolisa](https://arxiv.org/abs/1803.09885) - subset of Solidity
* [Logikon](https://github.com/logikon-lang/logikon) - an experimental language for smart contracts

No updates after 2017:
* [LLL](https://lll-docs.readthedocs.io/en/latest/) - a "low-level Lisp-like language" compiled to EVM bytecode ([discontinued](https://github.com/ethereum/solidity/blob/9abaa35d579ac982e77c811bbd007008f66cfd2e/Changelog.md#062-2020-01-27))
* [functional-solidity-language](https://github.com/raineorshine/functional-solidity-language) - pretty much self-descriptive :)
* [Serpent](https://github.com/ethereum/serpent/tree/ad53fa2a8a496448d58ef9137959b4a1e86b14d7) - a Python-like high-level language compiled to EVM (deprecated due to [security issues with the compiler](https://blog.zeppelin.solutions/serpent-compiler-audit-3095d1257929))
* [Babbage](https://medium.com/@chriseth/babbage-a-mechanical-smart-contract-language-5c8329ec5a0e) - "a mechanical smart contract language"
* [SolidityX](https://github.com/loomnetwork/solidityx-js) - a typed-superset of Solidity

No updates after 2016:
* [L4](https://youtu.be/Ufy8oM-Ou90) - a language "based on deontic modal logic", presented at Devcon 2 (Sep 2016)
* [Mutan](https://github.com/obscuren/mutan) - a C-like language compiled to EVM (deprecated)

## IRs
* [Yul](https://solidity.readthedocs.io/en/latest/yul.html) (ex JULIA, ex IULIA) - an intermediate language that can be compiled to bytecode for different backends.
* [Yul+](https://github.com/FuelLabs/yulp) - a low-level, highly efficient extension to Yul
* [SlithIR](https://github.com/crytic/slither/wiki/SlithIR) - an intermediate representation that is used by Slither to enable high-precision analysis via a simple API. It supports taint and value tracking to enable detection of complex patterns.
* [Elle](https://elle.readthedocs.io/en/latest/syntax.html#) - The Elle source language, also known as Elle-Core, captures structured programming abstractions and enables their translation to Ethereum EVM bytecode through a verified [compiler](https://elle.readthedocs.io/en/latest/implementation.html).

## DSLs

* [Alacrity](https://github.com/AlacrisIO/alacrity) - a DSL for simple, formally-verified DApps
* [Ergo](https://github.com/accordproject/ergo) - Domain specific language for smart legal contracts
* [Sandcastle](https://pegasys.tech/sandcastle-brings-sql-to-ethereum-smart-contracts/) - a SQL Ethereum smart contract language
* [FSolidM](https://github.com/anmavrid/smart-contracts/tree/FSMGenerator) - framework for [visual programming](https://cps-vo.org/group/smartcontracts) of Finite State Machines
* [Findel](https://github.com/cryptolu/findel) - a non Turing complete financial DSL inspired by a [S.P.Jones' work](https://www.microsoft.com/en-us/research/publication/composing-contracts-an-adventure-in-financial-engineering/)
* the language from [the paper](https://link.springer.com/article/10.1007/s12599-017-0507-z) by Egelund-Müller et al
* [Chorus](https://firmo.network/) - a financial contractual markup language by Firmo network
* [ADICO](https://papers.christopherfrantz.org/pdf/FrantzNowostawski2016_Smart_Contracts_nADICO.pdf) - a domain-specific language to support the contract modeling process
* [ink!](https://github.com/paritytech/ink) - an embedded DSL for writing WebAssembly based smart contracts using the Rust programming language and targeting Substrate blockchains. [Documentation](https://substrate.dev/docs/en/contracts/)
* [Reach](https://github.com/reach-sh/reach-lang) - a DSL for trustworthy DApps that enables junior developers without years of experience. [Documentation](https://docs.reach.sh/)

# Other blockchains

* [Move](https://developers.libra.org/docs/move-paper) - a safe and flexible programming language for the Libra Blockchain 
* [Michelson](http://www.michelson-lang.com/) - a stack based and strongly typed domain-specific language (Tezos)
* [Liquidity](http://www.liquidity-lang.org/) - a high-level typed smart-contract language that strictly complies to Michelson security restrictions (Tezos)
* [fi](https://github.com/TezTech/fi) (Tezos)
* [LIGO](https://medium.com/tezos/introducing-ligo-a-new-smart-contract-language-for-tezos-233fa17f21c7) (Tezos)
* [Plutus](https://github.com/input-output-hk/plutus) - a pure functional language with user-defined data types and polymorphism (Cardano); compiles to Plutus Core ([video](https://youtu.be/IqA-mI2olFA)) 
* [Marlowe](https://iohk.io/en/blog/posts/2018/12/11/marlowe-financial-contracts-on-blockchain/) - a domain-specific language for smart contract language embedded in Plutus (Cardano)
* [Rholang](https://github.com/rchain/rchain/tree/master/rholang) - a reflective higher-order process calculus language (RChain)
* [Obsidian](https://mcoblenz.github.io/Obsidian/) - a state-oriented language with linear types
* [DAML](https://daml.com/) - a smart contract language of Digital Asset
* [Simvolio](https://apla.io/) (Apla blockchain platform)
* [RIDE](https://wavesplatform.com/files/docs/white_paper_waves_smart_contracts.pdf) - a non Turing complete [language](https://docs.wavesplatform.com/en/technical-details/ride-language.html) infulenced by Scala and F# (Waves)
* [Scilla](https://scilla-lang.org) - an intermediate level language for verified smart contracts (Zilliqa)
* [TxVM](https://github.com/chain/txvm) (Chain)
* [IELE](https://github.com/runtimeverification/iele-semantics) - a variant of LLVM specialized to execute smart contracts on the blockchain
* [Pact](https://pact-language.readthedocs.io/en/stable/) - a smart contract language with a Lisp syntax but Haskell-like types (Kadena)
* [Ledger Design Language](https://eprint.iacr.org/2018/416) - a modeling language for describing public ledgers
* [Sigma-State](https://github.com/ScorexFoundation/sigmastate-interpreter) (Ergo)
* [Sophia](https://github.com/aeternity/protocol/blob/master/contracts/sophia.md) - a strongly typed language in the ML family (Æternity)
* [Varna](https://github.com/aeternity/protocol/blob/master/contracts/varna.md) - a non Turing complete high-level language (Æternity)
* [Fift](https://test.ton.org/fiftbase.pdf) - a stack-based general purpose programming language optimized for TON Blockchain smart contracts (TON)
* [Clarity](https://blog.blockstack.org/introducing-clarity-the-language-for-predictable-smart-contracts/) (Blockstack)
* [Ethermint](https://github.com/cosmos/ethermint) (Cosmos)
* [Secure EcmaScript](https://www.coindesk.com/cosmos-will-have-3-coding-languages-heres-why-that-matters-for-ethereum) (Cosmos)
* [Kadenamint](https://www.coindesk.com/cosmos-will-have-3-coding-languages-heres-why-that-matters-for-ethereum) (Cosmos)
* [Rell](https://rell.chromia.com/en/master/) (Chromia)
* [Solang](https://github.com/hyperledger-labs/solang) - a new Solidity compiler written in rust which uses llvm as the compiler backend. [Solang](https://solang.readthedocs.io/en/latest/) targets Substrate, Solana, ewasm, and Sawtooth. It is source compatible with Solidity 0.7
* [ConvexLisp](https://convex.world/cvm/data-types) (ConvexVM) - a Clojure-inspired decentralised smart contract language

# Other links

* https://github.com/pirapira/fp-ethereum - a collection of links related to function programming for Ethereum
* [Smart Contract Languages Development to Follow](https://blog.comae.io/smart-contract-languages-development-to-follow-992e30774b39) - a post by Matt Suiche, Comae (Dec 2017)
