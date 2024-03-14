# An AMM (automated market maker) Sui Move module

## Introduction

This Automated Market Maker (AMM) system is a decentralized exchange mechanism built on the Sui blockchain, leveraging the Move programming language. Designed to facilitate automated trading and liquidity provision, our AMM system employs a constant product formula `x * y = k` to ensure liquidity and enable seamless asset swaps within its ecosystem.

## About the Project

The core of this AMM system lies in its ability to create and manage liquidity pools for pairs of assets. It introduces concepts like liquidity pool coins (LP coins) which represent an individual's stake in a pool. The creation of a pool requires an initial liquidity supply, adhering to the `sqrt(amount_coin_a * amount_coin_b) - 1000` formula, ensuring a minimum liquidity threshold.

This project provides various functionalities including creating liquidity pools, adding or removing liquidity, and performing asset swaps through several methods like `swap_exact_a_for_b` or `swap_a_for_exact_b`, each catering to different trading strategies and ensuring efficient market operations.

## Getting Started

### Prerequisites

Ensure you have the following installed:
- [Sui Devnet Node](https://docs.sui.io/build/install)
- Move CLI for compiling and deploying smart contracts

### Installation and Configuration

1. **Clone the Repository**
    ```bash
    git clone https://github.com/ksmit323/liquidity-pool-move
    cd liquidity-pool-move
    ```

2. **Compile the Move Package**
    ```bash
    sui move compile
    ```

3. **Deploy to Sui**
    ```bash
    sui move publish
    ```

### Running the AMM System

- **Creating a Liquidity Pool**
    Utilize the `create_liquidity_pool` function with the initial asset amounts to establish a new liquidity pool.

- **Supplying Liquidity**
    Call `supply_liquidity` with the desired asset amounts to add liquidity to an existing pool.

- **Removing Liquidity**
    Use `remove_liquidity` and specify the LP coins you wish to redeem for underlying assets.

- **Swapping Assets**
    Engage in trades using functions like `swap_exact_a_for_b` to exchange assets at current market rates.

## Testing

To run the tests, use the following command:

```bash
sui move test
```

## Acknowledgement
This is the Pool Party quest given by Overmind

