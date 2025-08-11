<div align="center">

# **AcoreAI Subnet** <!-- omit in toc -->
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT) 

### Text-to-Speech,Emotion Rendering,3D interactions <!-- omit in toc -->
[Website](https://acore.app/) • [App](https://ai.acore.app/) • [Telegram](https://t.me/acoreai) • [Twitter](https://x.com/acore_ai)

![hero](./assets/acore-ai-subnet-banner.jpg)
</div>


## Introduction

AcoreAI is a Bittensor subnet dedicated to Text-to-Speech, Emotion Rendering, and 3D Interaction Generation using advanced AcoreAI network techniques. Our goal is to provide developers and artists with tools that simplify the creation of high quality Text-to-Speech, Emotion Rendering, and 3D interactions for various applications, including gaming, virtual reality, and simulations.

## Key Features

- **Subnet 405 (ACOREAI)**: Established as a dedicated marketplace for decentralized AI services, aligned with Bittensor’s architecture to reward high quality contributions.
- **Miners:**: Provide computational resources for text-to-speech, emotion rendering, and 3D interactions with photorealistic virtual agents.
- **Validators**: Evaluate service quality using Bittensor’s Yuma Consensus mechanism, ensuring fair rewards based on performance.
  
## AcoreAI Subnet Setup

This project outlines the steps to research, configure, and deploy a custom Bittensor subnet called **AcoreAI**. The goal is to understand the Bittensor and Subtensor frameworks and set up a local environment for development, including running a miner and validator.


# Miner and Validator Functionality

This tutorial shows how to  run incentives on it using the our testnet.
**important**.
- Do not expose your private key.
- Use only your testnet wallet.
- Do not reuse your mainnet wallet password.
- Make sure your incentives are resistant to abuse.

## Preparation
#### prepare subnet
```bash
git clone https://github.com/acoreai/subnet-acoreai
python3 -m venv btcli_venv
source btcli_venv/bin/activate

# setup bittensor sdk
pip install bittensor
pip install -e .
```
### start miner
```bash
python neurons/miner.py --netuid 405 --subtensor.network test --wallet.name miner --wallet.hotkey miner --logging.debug
```

### start validator
```bash
python neurons/validator.py --netuid 405 --subtensor.network test --wallet.name validator --wallet.hotkey validator --logging.debug 
```
### check state
```bash
btcli wallet overview --wallet.name miner --netuid 405 --subtensor.network test
btcli wallet overview --wallet.name validator --netuid 405 --subtensor.network test
```
