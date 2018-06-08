Robonomics communication stack 
==============================
[![Build Status](https://travis-ci.org/airalab/robonomics_comm.svg?branch=master)](https://travis-ci.org/airalab/robonomics_comm)
![BSD3 License](http://img.shields.io/badge/license-BSD3-brightgreen.svg)

> This is reference implementation of robot economics protocol.

Robonomics communication stack contains a set of ROS packages for economical communication purposes.

**Installation** process is similar to any ROS catkin package set.

```bash
mkdir -p ws/src && cd ws/src
git clone https://github.com/airalab/robonomics_comm
catkin_init_workspace && cd .. && catkin_make 
```
Robonomics lighthouse 
-----------------

Lighthouse package implements protocol part about robonomics lighthouses functionality:
markets, orders, deals, liabilities, results. The decentralized robonomics markets
use IPFS and Ethereum smart contracts for order processing.


Robonomics liability
--------------------

Liability package implements protocol part about robot liability
smart contract actions. It provide methods for robot task/result
store, delivery and interpretation.

Robonomics control
------------------

This packages implements robonomics control rules described at [article](http://ensrationis.com/smart-factory-and-capital/).

Examples
--------

**Client**

```bash
$ roslaunch robonomics_lighthouse infochan.launch
```

**Lighthouse**

```bash
$ roslaunch robonomics_lighthouse lighthouse.launch
```

**Robot**

```bash
$ roslaunch robonomics_liability liability.launch
```
