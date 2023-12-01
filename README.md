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

#### Примечание 
Protostar требует версию Git 2.28 или выше.


### Установка зависимостей Protostar
```
protostar install
```

### Компиляция контрактов
```
protostar build
```

### Запуск тестов
```
protostar test
```

### Запуск скриптов


#### Установка локального виртуального окружения

```
python -m venv ./venv
source ./venv/bin/activate
```

#### Установка зависимостей
```
pip install -r requirements.txt
```

Больше информации об устанавливемых зависимостях можно найти тут:
* [starknet-devnet](https://github.com/Shard-Labs/starknet-devnet)
* [starknet.py](https://github.com/software-mansion/starknet.py)


#### Запуск скриптов

Все скрипты находятся в директории ```scripts```. Конфигурационный файл отсутсвует, пожалуйста, создайте свой в ```scripts/config```

Для запуска скриптов налокальной системе вам сначала нужно запустить devnet-сервер:
```
starknet-devnet
```

Run script by specifying the path to the script file. Example:
```
python scripts/deploy.py local
```
