# Blocktrails Playground

NATEOS - Nostr As The Engine Of State

Live viewer for [blocktrails](https://github.com/blocktrails/blocktrails) state sync.

## Usage

Open `index.html` with URL params:

```
?pubkey=<hex>     Filter to specific trail
?relay=<url>      Custom relay (default: wss://relay.damus.io)
```

## How it works

1. Connects to Nostr relay
2. Subscribes to kind 30333 (blocktrail) events
3. Parses latest state as hue (0-360)
4. Sets background color

## Demo

```bash
# Terminal
bt genesis 180
bt publish

# Browser
open index.html?pubkey=<your-pubkey>

# Update
bt advance 280
bt publish
# → background changes to purple
```
