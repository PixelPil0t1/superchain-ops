# 010-opcm-update-prestate-v300-op-ink: Sepolia Update Prestate v3.0.0: OP and Ink

Status: [EXECUTED](https://sepolia.etherscan.io/tx/0x659ca2fe3231cdda8657ff4e0bc11f7dfd7345413d4f854d3a53c5036fce3732)

## Objective

Executes [Upgrade 15](https://gov.optimism.io/t/upgrade-proposal-15-isthmus-hard-fork/9804) on OP Sepolia and Ink Sepolia.

This task uses `op-contract/v3.0.0` [OPContractsManager](https://github.com/ethereum-optimism/optimism/blob/op-contracts/v3.0.0-rc.2/packages/contracts-bedrock/src/L1/OPContractsManager.sol) to update the prestates of 2 chains:

1. OP Sepolia Testnet
2. Ink Sepolia Testnet

### Timing

Expected to be executed on or around 2025-04-11.

## Transaction creation

The transaction is generated by the [OPCMUpdatePrestateV300 template script](../../../template/OPCMUpdatePrestateV300.sol),
which reads the inputs from the [`config.toml`](./config.toml) file.

## Signing and execution

Follow the instructions in the [Nested Execution](../../../NESTED.md) guide for the following steps:

- [1. Update repo](../../../NESTED.md#1-update-repo)
- [2. Setup Ledger](../../../NESTED.md#2-setup-ledger)
- [3. Simulate and validate the transaction](../../../NESTED.md#3-simulate-and-validate-the-transaction)

Then follow the instructions in the [Validation](./VALIDATION.md) guide.

## Simulation

When simulating, ensure the logs say `Using script <your_path_to_superchain_ops>/superchain-ops/src/improvements/template/OPCMUpdatePrestateV300.sol`.
Navigate to the correct task directory then run the simulate command.
```
cd src/improvements/tasks/sep/010-opcm-update-prestate-v300-op-ink
SIMULATE_WITHOUT_LEDGER=1 just --dotenv-path $(pwd)/.env --justfile ../../../nested.just simulate <foundation|council>
```
