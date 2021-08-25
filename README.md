# Perfectly Balanced

![image](https://user-images.githubusercontent.com/88283485/130841235-3e8901c5-3477-4107-b15f-f284a06a9665.png)

Script to make your LND node pefectly balanced as all things should be.

## Requirements:

- rebalance-lnd: https://github.com/C-Otto/rebalance-lnd (If you can run it we are good)
- bc: https://www.gnu.org/software/bc/manual/html_mono/bc.html (Install your distro package)

## Usage

Edit these values according to your node:

```
Your settings vars:

REBALANCE_LND_FILEPATH=/home/umbrel/Downloads/rebalance-lnd/rebalance.py
LND_DIR=/mnt/umbrel/Umbrel/lnd/
MAX_FEE=100
TOLERANCE=0.999 # I do not recommend to put 1 here, it may get crazy XD

# Your channels to keep perfectly balanced, get them with `rebalance.py -l -c`
# See https://github.com/C-Otto/rebalance-lnd for more info

declare -a channels=(
  766511337228992513 # SpaintoLATAM
  766880773108203521 # renoblitz
  766283738386399232 # 02a446876eafbbdaa96e
  765011603400949760 # Gondolin
  765016001414299649 # rbvdr21
  766262847645417473 # 031b0b9df8e34e53de02
  766874176095649792 # LibertyBull
  766898365405003777 # Plaidfunds
  761111635631734784 # 02c603d30ea3711144d4
  766534426924810241 # Cuerna
)

# Liquidity channels also included in `reb -l -c` but you use these channels to pump and dump sats

LIQUIDITY_PUMP=766237558887612417 # LNBIG.com [lnd-03]
LIQUIDITY_DUMP=761128128258703361 # LNBIG.com [lnd-13]
```

## Example

![image](https://user-images.githubusercontent.com/88283485/130842915-43e6a401-6089-40f4-b625-72867f7dc11d.png)

## Contribute

- Also feel free to collaborate with code or donate a few Satoshi using your LND Lightning node ⚡ 😄

```
./lncli sendpayment --keysend 03e7299ced214b19b87ed87979462d9aee3ec07a42fe6e2211854bfa4cb32b0bb8 10 # sats
```
