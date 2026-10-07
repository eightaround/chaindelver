# ChainDelver

_A provably-fair roguelike dungeon crawler where every run and death is permanently on-chain_

## Summary

ChainDelver is a single-player roguelike where the dungeon layout, loot drops, and permadeath outcomes are generated using on-chain verifiable randomness, so players can trust the game is never rigged. Each character is an NFT that evolves across runs, and when it dies, a permanent 'Trophy NFT' records its final stats and depth reached, creating a provable history of the player's best runs.

## Target users

Solo roguelike/dungeon-crawler fans who value fairness and provable achievements

## Problem

Players can't trust that loot drops or random events in most games are truly fair, and achievements are easily faked or lost when servers shut down.

## Solution

Use on-chain VRF for all randomness and mint permanent NFTs recording run outcomes, so fairness and achievements are verifiable and permanent.

## MVP features

- 2D dungeon crawler built in Phaser/Godot with wallet login
- On-chain VRF (Switchboard) seeds dungeon layout and loot drops each run
- Character NFT stores persistent stats (level, gold, best depth) on Solana
- Permadeath mints a 'Trophy NFT' recording final stats and run history
- On-chain leaderboard ranking players by deepest run reached

## Chains

Solana

## Tech

Anchor, Switchboard VRF, Phaser.js, Solana Wallet Adapter, TypeScript, Metaplex

## Category

Gaming

## Why now

Solana's low fees and fast finality make it feasible to write frequent game-state updates on-chain without breaking the gameplay loop.

## Roadmap

- Add procedurally generated boss fights and biome variety
- Introduce seasonal leaderboards with cosmetic NFT rewards
- Expand to mobile client for wider accessibility
