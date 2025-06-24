### Knots node list updated June 22, 2025
---
<i></u><b>Why would I want to ban Knots nodes?</b></i>
<br>
By default, Knots nodes implement a highly restrictive relay policy that attempts to prevent specific valid transactions from propagating through the Bitcoin network. This means that if your node is connected to a majority of Knots nodes, it will hinder your node’s ability to estimate fees properly and increase the time it takes for your node to receive new blocks
<br><br>

If you would like to apply this banlist to your node:
1. Stop your Bitcoin node.
2. Navigate to your main Bitcoin directory (where your bitcoin.conf file is).
3. Save and copy the "banlist.json" file from this repository to your Bitcoin directory.
4. Start your Bitcoin node.

<i>Note: Using this banlist will overwrite any existing banlist.json in your Bitcoin directory. If you already have entries in your banlist.json, simply copy them to this new banlist.json.</i>



<br>
Knots node list was sourced from: https://bitnodes.io/api/v1/snapshots/latest/

I2P nodes are added manually. Feel free to submit a PR for any missing nodes.
