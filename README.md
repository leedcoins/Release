# Release Linux Ubuntu 18.04(64-bit)
How do I setup a node on Ubuntu Server 18.04?
Install Ubuntu Server 18.04 on a VPS.

Update your Ubuntu machine.
sudo apt-get update
sudo apt-get upgrade

Install the required dependencies.

sudo apt-get install build-essential libtool autotools-dev automake pkg-config libssl-dev libevent-dev bsdmainutils python3 libboost-system-dev libboost-filesystem-dev libboost-chrono-dev libboost-test-dev libboost-thread-dev libboost-all-dev libboost-program-options-dev zip

sudo apt-get install libminiupnpc-dev libzmq3-dev libprotobuf-dev protobuf-compiler unzip software-properties-common

Install Berkeley DB.

sudo add-apt-repository ppa:bitcoin/bitcoin
sudo apt-get update
sudo apt-get install libdb4.8-dev libdb4.8++-dev

Download the daemon and tools from LeedCoin.

wget "https://github.com/leedcoins/Release/raw/master/leedcoin-linux.zip"

Extract the tar files.

sudo unzip leedcoin-linux.zip

Install the daemon and tools.

cd /leedcoin-linux

sudo mv leedcoind leedcoin-cli leedcoin-tx leedcoin-qt /usr/bin/

Create the config file.

mkdir $HOME/.leedcoin

nano $HOME/.leedcoin/leedcoin.conf

Paste the following lines in examplecoin.conf

rpcuser=rpc_leedcoin
rpcpassword=123456789
rpcallowip=127.0.0.1
listen=1
server=1
txindex=1
daemon=1

Start your node with the following command.

leedcoind
