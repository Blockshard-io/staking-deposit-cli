# **Generate Valid Hoodi Validator Keys**

This repository provides a modified version of `staking-deposit-cli` that supports the **Hoodi testnet**. Follow the steps below to generate valid Ethereum validator keys for Hoodi.

---

## **1. Clone This Repository**
To use this version of `staking-deposit-cli`, clone this repository:

```bash
git clone https://github.com/Blockshard-io/staking-deposit-cli.git
cd staking-deposit-cli
git checkout hoodi
```

---

## **2. Install Python and Set Up Environment**
To run `staking-deposit-cli`, you need **Python 3.8+** installed. If Python is not installed, follow these steps:

### **Install Python (Ubuntu/Debian)**
```bash
sudo apt update
sudo apt install python3 python3-venv python3-pip -y
```

---

## **3. Set Up a Python Virtual Environment**
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

## **4. Generate Validator Keys for Hoodi**
Once the environment is set up, generate validator keys using:

```bash
python3 deposit.py new-mnemonic --num_validators 1 --chain hoodi --eth1_withdrawal_address <YourWithdrawalAaddress>
```

Replace `1` with the number of validators you want to generate.

This command will:
- Generate **a new mnemonic**.
- Create validator **keystore files**.
- Generate a **deposit_data.json** file.

---

## **5. Submit Your Deposit Using Dora Hoodi Explorer**
Once you have `deposit_data.json`, you need to submit your deposit to the **Hoodi Deposit Contract** using the **Dora Hoodi Explorer**.

1. **Go to** [Dora Hoodi Explorer](https://dora.hoodi.ethpandaops.io/validators/deposits/submit).
2. **Connect your wallet** that holds at least **32 HoodiETH per validator**.
3. **Upload your `deposit_data.json` file**.
4. **Submit the transaction** using your wallet.

After submission, the deposit transaction will be processed and will appear on the Hoodi Beacon Chain [here](https://dora.hoodi.ethpandaops.io/validators/deposits).
