# hubot-ama

A hubot plugin that hosts AMAs.

See [`src/ama.coffee`](src/ama.coffee) for full documentation.

## Usage

* `ama start` - pick someone for an AMA and repeat every 24 hours
* `ama stop` - stop picking AMAs every 24 hours
* `ama current` - display the current AMA celebrity
* `ama pass` - stops the ama and returns the selected candidate's weight to the previous value
* `ama add` - add yourself to the AMA list
* `ama remove` - remove yourself from the AMA list
* `ama list` - lists all AMA candidates
* `ama odds` - shows odds of each candidate being chosen
* `ama clear` - clears selections (admin only)

## Installation

In hubot project repo, run:

`npm install hubot-ama --save`

Then add **hubot-ama** to your `external-scripts.json`:

```json
["hubot-ama"]
```

The plugin by default only works in channels called #bots, for testing, and #ama. To change that, fork the repo and modify ama.coffee. Also, the admins are by default a set of people who have contributed to this in our personal Slack - the only command you need admin abilities is `ama clear`, so it should run fine without modification, unless you need that specific command (we've only had to use it once, and that was to after some heavy modifications to the script and changed the way we stored the user list). Again, to change the admins, simply fork the repo and modify the script.
