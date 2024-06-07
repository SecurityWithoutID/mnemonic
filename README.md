# mnemonic
Generate mnemonic with self-chosen entropy

## Steps
optional: use an amnesic VM for safety

```
$ sudo apt install python3-pip
$ pip3 install mnemonic
```

optional: now disable networking for safety

```
$ python3
>>> import hashlib
>>> from mnemonic import Mnemonic
```

choose a `CASE_SENSTIVE_INPUT_STRING` with enough entropy to be a private key

```
>>> inputString = 'CASE_SENSTIVE_INPUT_STRING'
>>> m = Mnemonic("english")
>>> m.to_mnemonic(hashlib.sha256(inputString.encode('utf-8')).digest())
```

the last line outputs the mnemonic
