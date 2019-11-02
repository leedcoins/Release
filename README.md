# Release Linux Ubuntu 18.04(64-bit)
How do I setup a node on Ubuntu Server 18.04?
Install Ubuntu Server 18.04 on a VPS.

Update your Ubuntu machine.
sudo apt-get update
sudo apt-get upgrade

Install the required dependencies.
sudo apt-get install build-essential libtool autotools-dev automake pkg-config libssl-dev libevent-dev bsdmainutils python3 libboost-system-dev libboost-filesystem-dev libboost-chrono-dev libboost-test-dev libboost-thread-dev libboost-all-dev libboost-program-options-dev
sudo apt-get install libminiupnpc-dev libzmq3-dev libprotobuf-dev protobuf-compiler unzip software-properties-common

Install Berkeley DB.

sudo add-apt-repository ppa:bitcoin/bitcoin
sudo apt-get update
sudo apt-get install libdb4.8-dev libdb4.8++-dev

Download the daemon and tools from LeedCoin.
wget "https://github.com/leedcoins/Release/raw/master/leedcoin-linux.zip
