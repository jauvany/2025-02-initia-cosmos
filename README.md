# Initia Cosmos audit details
- Total Prize Pool: $80,000 in USDC
  - HM awards: $51,500 in USDC
  - QA awards: $2,100 in USDC
  - Judge awards: $6,200 in USDC
  - Validator awards: $4,200 in USDC
  - Mitigation Review: $16,000 in USDC
- [Read our guidelines for more details](https://docs.code4rena.com/roles/wardens)
- Starts February 10, 2025 20:00 UTC
- Ends February 24, 2025 20:00 UTC

**Note re: risk level upgrades/downgrades**

Two important notes about judging phase risk adjustments: 
- High- or Medium-risk submissions downgraded to Low-risk (QA) will be ineligible for awards.
- Upgrading a Low-risk finding from a QA report to a Medium- or High-risk finding is not supported.

As such, wardens are encouraged to select the appropriate risk level carefully during the submission phase.

## Automated Findings / Publicly Known Issues

_Note for C4 wardens: Anything included in this `Automated Findings / Publicly Known Issues` section is considered a publicly known issue and is ineligible for awards._

- Already known issue in cosmos-sdk is not target of this audit.
- In some places, we are raising panic but it is normally okay to ignore. Especially if it is coming from the https://github.com/cosmos/cosmos-sdk. (x/mstaking, x/gov, x/bank, x/evidence).
- Dependency versions are also not a target of this audit.

## Links

- **Previous audits:**  https://github.com/Zellic/publications/blob/master/Initia%20-%20Zellic%20Audit%20Report.pdf
- **Documentation:** https://initialabs-develop.mintlify.app/
- **Website:** https://initia.xyz/
- **X/Twitter:** https://x.com/initia
- **Discord:** https://discord.gg/initia

---

# Scope

## Files in scope

**Initia**
- Source code location: https://github.com/initia-labs/initia/
- Source code version: [e74fb02397a541faed07fb3488ad2618808967b5](https://github.com/initia-labs/initia/commit/e74fb02397a541faed07fb3488ad2618808967b5)
- Files:
  - x/bank/**
  - x/distribution/**
  - x/ibc/*
  - x/move/*
  - x/ibc-hooks/*
  - x/mstaking/*
  - x/reward/*


**MiniWasm**
- Source code location: https://github.com/initia-labs/miniwasm
- Source code version: [ed1728e2ad51f214ee0191dde62d96a074f55f1f](https://github.com/initia-labs/miniwasm/commit/ed1728e2ad51f214ee0191dde62d96a074f55f1f)
- Files:
 - x/bank/**
 - x/tokenfactory/**
 - app/**

 **MiniEVM**
- Source code location: https://github.com/initia-labs/minievm
- Source code version: [744563dc6a642f054b4543db008df22664e4c125](https://github.com/initia-labs/minievm/commit/744563dc6a642f054b4543db008df22664e4c125)
- Files:
 - x/evm/**
 - x/bank/**
 - jsonrpc/**
 - indexer/**

## Main invariants

* We can trust governance account.

## Attack ideas (where to focus for bugs)
non-deterministic state changes

## All trusted roles in the protocol

Governance Account

## Running tests

# initia
git clone https://github.com/initia-labs/initia
(cd initia && make test)

# minimove
git clone https://github.com/initia-labs/minimove
(cd minimove && make test)

# miniwasm
git clone https://github.com/initia-labs/miniwasm
(cd miniwasm && make test)

# minievm
git clone https://github.com/initia-labs/minievm
(cd minievm && make test)

## Miscellaneous
Employees of Initia and employees' family members are ineligible to participate in this audit.

Code4rena's rules cannot be overridden by the contents of this README. In case of doubt, please check with C4 staff.



