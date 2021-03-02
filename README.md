# Tezos-Project

## Introduction :
Contract de vote en Tezos.

## Installation et Utilisation :
Tout d'abord installer Ligo :
+ [Tezos - Installation](https://tezos.gitlab.io/introduction/howtoget.html#build-from-sources)
+ [LIGO Lang - Installation](https://ligolang.org/docs/intro/installation/)

Ensuite déployer le contract `votingContract.ligo` :
```
ligo compile-contract votingContract.ligo main > votingContract.tz
```
```
ligo compile-storage votingContract.ligo main 'record admin = ("tz1LKe9GQfF4wfob11YjH9grP1YdEWZtPe9W": address); paused = False; votes = (map[] : map(address, bool)); end'
```
```
ligo compile-parameter votingContract.ligo main "Vote(record vote = False; end)" 
ligo compile-parameter votingContract.ligo main "Reset(0)"
```
```
pytest pyTestContract.py
```
