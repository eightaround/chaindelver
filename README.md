# ChainDelver
![ChainDelver logo](assets/logo.png)

A provably-fair roguelike dungeon crawler where every run and death is permanently on-chain.

## Overview

ChainDelver is a single-player roguelike dungeon crawler built on Solana. Dungeon layouts, loot drops, and permadeath outcomes are generated using on-chain verifiable randomness, so players never have to trust a hidden server-side RNG. Characters are NFTs that evolve across runs, and every death mints a permanent Trophy NFT recording the character's final stats and depth reached.

## Problem

Players can't trust that loot drops or random events in most games are truly fair, because the randomness happens on a server they can't inspect. Achievements are easily faked, altered, or simply lost forever when a game's servers shut down.

## Solution

ChainDelver replaces hidden server RNG with on-chain verifiable randomness (Switchboard VRF) for every dungeon seed and loot drop. Character progress and permadeath outcomes are recorded on-chain as NFTs, creating a permanent, provable history of every run that cannot be altered or lost.

## Features (MVP)

- 2D dungeon crawler built in Phaser with Solana wallet login
- On-chain VRF (Switchboard) seeds dungeon layout and loot drops each run
- Character NFT stores persistent stats (level, gold, best depth) on Solana
- Permadeath mints a Trophy NFT recording final stats and run history
- On-chain leaderboard ranking players by deepest run reached

## Tech Stack

- Anchor (Solana smart contracts)
- Switchboard VRF (verifiable randomness)
- Phaser.js (2D game client)
- Solana Wallet Adapter
- TypeScript
- Metaplex (NFT standards)

## How It Works

```
[Player + Wallet]
 |
 v
[Phaser Game Client] ----request VRF----> [Switchboard Oracle]
 |                                            |
 | reads seed                                 | returns verifiable randomness
 v                                            v
[Anchor Program on Solana] <-------------------
 |
 |--> updates Character NFT (level, gold, best depth)
 |--> on permadeath: mints Trophy NFT (final stats, run history)
 |--> updates on-chain leaderboard
```

Each run starts with a wallet-signed request for a verifiable random seed from Switchboard. That seed deterministically generates the dungeon layout and loot drops client-side, so outcomes can be independently verified. Character state and run outcomes are written to an Anchor program on Solana, keeping stats, Trophy NFTs, and the leaderboard permanent and tamper-proof.

## Roadmap

- Add procedurally generated boss fights and biome variety
- Introduce seasonal leaderboards with cosmetic NFT rewards
- Expand to mobile client for wider accessibility

## Pitch

- [Pitch deck (PDF)](docs/pitch.pdf)
- [Pitch script](docs/pitch-script.md)

## Team

- Name / role (placeholder)
- Name / role (placeholder)
- Name / role (placeholder)

Built for the Colosseum hackathon.

---

🎬 Pitch video: [docs/pitch-video.mp4](docs/pitch-video.mp4)


## Prototype

Live prototype: https://eightaround.github.io/chaindelver/

The source is [docs/index.html](docs/index.html) (served with GitHub Pages from the /docs folder). All data is simulated.
