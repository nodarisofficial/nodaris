# Nodaris Mining Guide (Android Termux / Linux)

Status: draft. Launch not announced yet.

## 1. Install
Install Termux from F-Droid, then:

    pkg install -y libevent sqlite python
    mkdir -p ~/nodaris && cd ~/nodaris
    tar xzf nodaris-*.tar.gz

(Download link will be published at launch.)

## 2. Start the node

    termux-wake-lock
    ./nodarisd -daemon -addnode=SEED_IP:19333
    ./nodaris-cli getblockchaininfo

Wait until "blocks" matches the network height.

## 3. Create a wallet

    ./nodaris-cli createwallet miner
    ./nodaris-cli getnewaddress
    ./nodaris-cli backupwallet ~/miner-backup.dat

Keep two copies of the backup in different places. If you lose your keys, your coins are gone forever.

## 4. Mine

    python nminer.py YOUR_ADDRESS 2

The last number is CPU threads. Use fewer if your phone gets hot. Stop with Ctrl+C.

## 5. Good habits
- Stop the node with `./nodaris-cli stop`, never by closing Termux.
- Mined coins can be spent after 100 blocks.
- Mining heats the phone: keep it on a charger and in a cool place.
- Nothing here is investment advice. NDRS has no guaranteed value.
