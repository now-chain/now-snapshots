# Usage
## Step 1: Preparation
- A disk with enough free storage, at least twice the size of the snapshot.

## Step 2: Download
- Copy the above snapshot URL.
- Run: `nohup wget "<paste snapshot URL here>" <your dir> &`

## Step 3: Uncompress
- Uncompress will take more time, put it in the background by `nohup tar -xzvf geth.tar.gz &`


## Step 4: Replace Data
- First, stop the running NOW client if you have one by `kill {pid}`, and make sure the client has shut down.
- Consider backing up the original data if needed: `mv ${NOW_DataDir}/geth/chaindata ${NOW_DataDir}/geth/chaindata_backup`
- Replace the data: `mv geth/chaindata ${NOW_DataDir}/geth/chaindata`
- Start the NOW client again and check the logs