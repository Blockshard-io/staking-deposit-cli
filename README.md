
# **Generating Valid Hoodi Validator Keys**

This repository provides a modified version of `staking-deposit-cli` that supports the **Hoodi testnet**. Follow the steps below to generate valid Ethereum validator keys for Hoodi.

---

## **1. Clone This Repository**
To use this version of `staking-deposit-cli`, clone this repository:

```bash
git clone https://github.com/Blockshard-io/staking-deposit-cli.git
cd staking-deposit-cli
```

---

## **2. Set Up Python Environment**
To avoid dependency conflicts, create and activate a **Python virtual environment**:

```bash
python3 -m venv venv
source venv/bin/activate
```

Then, install the required dependencies:

```bash
pip install -r requirements.txt
```

---

## **3. Generate Validator Keys for Hoodi**
Once the environment is set up, generate validator keys using:

```bash
python3 deposit.py new-mnemonic --num_validators 1 --chain hoodi
```

Replace `1` with the number of validators you want to generate.

This command will:
- Generate **a new mnemonic**.
- Create validator **keystore files**.
- Generate a **deposit_data.json** file.



If you encounter any issues, open an **issue on GitHub** or join the **Hoodi community channels** for assistance. 🚀
