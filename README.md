### Knots banlist updated July 26, 2025
Knots node address list is sourced from: https://bitnodes.io/api/v1/snapshots/latest/

I2P and previously known nodes were added manually.
Feel free to submit a PR for any missing nodes.

---

### To apply this banlist to your node:

1. Stop your Bitcoin node.
2. Navigate to your main Bitcoin directory (where your ```bitcoin.conf``` file is).
3. Save and copy the ```banlist.json``` file from this repository to your Bitcoin directory.
4. Start your Bitcoin node.

<b>Caveat: Bitcoin nodes handle Tor connections in such a way that will still allow Knots nodes to connect to your node as inbound peers. To prevent this set the following flags in your ```bitcoin.conf``` file: ```listenonion=0``` and ```i2pacceptincoming=1``` </b>

<i>Note: This banlist file will overwrite any existing banlist file in your Bitcoin directory. If you already have a banlist file, simply copy its contents to this new one.</i>
<br>

---
### Why would I want to ban Knots nodes?

By default, Knots nodes implement a highly restrictive relay policy that attempts to prevent specific valid transactions from propagating through the Bitcoin network. This means that if your node is connected to a majority of Knots nodes, it will hinder your node’s ability to estimate fees properly and increase the time it takes for your node to receive new blocks
<br>

---
### Build Your Own:

If you would like to build your own ```banlist.json``` based on the bitnodes.io API, you can run the provided ```knotsban.py``` script. The script will fetch all current Knots nodes from bitnodes.io and output a ```banlist.json``` file.

<i>Note: bitnodes.io does not list I2P Knots nodes, so any manually generated lists will not include them.</i>

To mitigate this, use ```knownknots.txt``` alongside the ```knotsban.py``` script. The script will compare the list of addresses in ```knownknots.txt``` and output a ```banlist.json``` file containing all the previously known addresses combined with any new ones found by the bitnodes API.
