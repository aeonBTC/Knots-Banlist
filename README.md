### Knots banlist updated January 5, 2026
Knots node address list is sourced from: https://bitnodes.io/api/v1/snapshots/latest/

<i>Note: I2P nodes are not included in this list. I2P nodes generate new addresses for every inbound/outbound connection and are not easily banned.

To mitigate this open your ```bitcoin.conf``` file, add ```i2pacceptincoming=0``` and delete ```onlynet=i2p```.</i>

---

### Why would I want to ban Knots nodes?

By default, Knots nodes implement a highly restrictive relay policy that attempts to prevent specific valid transactions from propagating through the Bitcoin network. This means that if your node is connected to a majority of Knots nodes, it will hinder your node’s ability to estimate fees properly and increases the time it takes for your node to validate new blocks
<br>

---
### To apply this banlist to your node:

1. Navigate to your main Bitcoin directory (where your ```bitcoin.conf``` file is).
2. Save and copy the ```banlist.json``` file from this repository to your Bitcoin directory.

<i>Note: This banlist file will overwrite any existing banlist file in your Bitcoin directory. If you already have a banlist file, simply copy its contents to this new one.</i>
<br>

---

### Build Your Own:

If you would like to build your own ```banlist.json``` based on the bitnodes.io API, you can run the provided ```knotsban.py``` script. The script will fetch all current Knots nodes from bitnodes.io and output a ```banlist.json``` file.


