# JediSwap

Клон of Uniswap V2 на Cairo. AMM для StarkNet.

## Тестирование и разработка

Мы используем [Protostar](https://docs.swmansion.com/protostar/) для наших тестировочных и разработчиковских нужд.

Protostar - это набор для разработки смарт-контрактов на StarkNet, который помогает с управлением зависимостями, компилированием и тестированием контрактов на Cairo. 

### Установка Protostar


1. Скопируйте и запустите в терминале следующую команду:
```
curl -L https://raw.githubusercontent.com/software-mansion/protostar/master/install.sh | bash
```
2. Перезапустите терминал.
3. Запустите команду `protostar -v` для проверки версий Protostar и cairo-lang.

#### Note 
Protostar requires version 2.28 or greater of Git.


### Install Protostar Dependencies
```
protostar install
```

### Compile Contracts
```
protostar build
```

### Run Tests
```
protostar test
```

### Run Scripts


#### Setup a local virtual env

```
python -m venv ./venv
source ./venv/bin/activate
```

#### Install dependencies
```
pip install -r requirements.txt
```

Find more info about the installed dependencies here:
* [starknet-devnet](https://github.com/Shard-Labs/starknet-devnet)
* [starknet.py](https://github.com/software-mansion/starknet.py)


#### Run Scripts

All scripts are placed in ```scripts``` folder. testnet config is not committed, please create your own in ```scripts/config```

To run scripts on local system, you first need to run a devnet server:
```
starknet-devnet
```

Run script by specifying the path to the script file. Example:
```
python scripts/deploy.py local
```
