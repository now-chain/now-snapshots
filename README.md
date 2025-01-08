
# About NOW Snapshots

## Source: Legacy Full Node(> 1TB)
Usage: [usage/legacyfullnode_usage.md](./usage/legacyfullnode_usage.md)

### Mainnet (monthly update)

Full Snapshot: [mainnet-now-20250108](dist/mainnet_now_20250108.tar.gz)

## FAQ

### Why split snapshot into multiple files?

As the node snapshot of bsc becomes larger and larger, backup, upload and download will become increasingly unmaintainable, and it will occupy more disk space and take up more upload and download time.

At the same time, in order to support the history expiry and state expiry of bsc later, it is planned to split the node snapshot according to historical data and active data, and the following advantages can be obtained:

1. When updating the snapshot, only the changed part can be updated to reduce the difficulty of operation and maintenance;
2. Support annual backup of historical data, which also helps with the subsequent historical data pruning;
3. Support archiving multiple snapshot versions, avoiding wasting disk space;
4. Support downloading and decompressing a single part immediately, and snapshot download and decompression can be completed on a smaller disk;