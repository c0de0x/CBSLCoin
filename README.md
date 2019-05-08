CbslCoin Core (fork of PIVX) integration/staging repository
======================================

OUR MAINNET LAUNCH at 3 May 2019

to get more info : https://discordapp.com

It is recommended [use the shell script](https://github.com/CBLdev123/Masternode-install) to install a CBSL Masternode on a Linux server running Ubuntu 14.04 or 16.04

***

Quick installation of the CBSL daemon under linux. See detailed instructions there [build-unix.md](build-unix.md)

Installation of libraries (using root user):

    add-apt-repository ppa:bitcoin/bitcoin -y
    apt-get update
    apt-get install -y build-essential libtool autotools-dev automake pkg-config libssl-dev libevent-dev bsdmainutils
    apt-get install -y libboost-system-dev libboost-filesystem-dev libboost-chrono-dev libboost-program-options-dev libboost-test-dev libboost-thread-dev
    apt-get install -y libdb4.8-dev libdb4.8++-dev

Cloning the repository and compiling (use any user with the sudo group):

    cd
    git clone https://github.com/CBLdev123/CBSLCoin.git
    cd CBSL
    ./autogen.sh
    ./configure
    sudo make install
    cd src
    sudo strip CBSLd
    sudo strip CBSL-cli
    sudo strip CBSL-tx
    cd ..

Running the daemon:

    CBSLd 

Stopping the daemon:

    CBSL-cli stop

Demon status:

    CBSL-cli getinfo
    CBSL-cli mnsync status

All binaries for different operating systems, you can download in the releases repository:

https://github.com/CBLdev123/CBSLCoin/releases

P2P port: 28864, RPC port: 25563
-
Distributed under the MIT software license, see the accompanying file COPYING or http://www.opensource.org/licenses/mit-license.php.
