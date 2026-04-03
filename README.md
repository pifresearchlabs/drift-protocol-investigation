# Drift Protocol Exploit — On-Chain Investigation

### PIF Research Labs

**$285M drained in 10 seconds. We traced every dollar.**

---

On April 1, 2026, the Drift Protocol exploit drained $285M from Solana vaults in 10 seconds using a fake collateral market, a compromised admin key, and pre-signed durable nonce transactions. The attacker dispersed funds across 50,000+ wallets on five chains. This is the full on-chain forensic reconstruction.

---

## The Investigation

### [Main Infographic — Full Exploit Reconstruction](https://pifresearchlabs.github.io/drift-protocol-investigation/pif-drift-notion-infographic.html)

The complete forensic breakdown of the Drift Protocol exploit from start to finish. Covers the 20-day setup (CVT token mint, $1 rehearsal, durable nonce pre-signing), the multisig takeover (2/5 threshold, 0-second timelock, admin key transferred in 1 second), the weaponization (fake collateral market, disabled circuit breakers raised 100,000x), the 10-second drain ($233M across 18 token types, JLP vault 99.9997% emptied), the CCTP bridge pipeline ($463M USDC burned on Solana, minted on Ethereum through Circle's own contracts), the Ethereum conversion ($125M swapped to ETH through CowSwap and 0x Settler), the four ETH vault wallets (130,262 ETH, ~$278M, zero outbound), the Solana dispersion network (364,000+ transactions, 2,600+ wallets, bot running 52+ hours), and the Binance cashout ($525M+ deposited across 92 transactions). Every number verified on-chain.

---

### [Show Me The Money — Post-Heist Fund Location Map](https://pifresearchlabs.github.io/drift-protocol-investigation/pif-show-me-the-money.html)

Where is every dollar right now? This is the post-heist forensic map updated in real time as the attacker moves funds. Tracks four ETH vault wallets holding 130,262 ETH (~$278M) with zero outbound transactions, $525M+ deposited to Binance through a CCTP mint-to-deposit pipeline that started 86 minutes before the drain, the Solana dispersion bot still running at 52+ hours with 364,000+ transactions, and new CCTP minting wallets appearing daily. Drift sent on-chain messages to all four vault wallets on April 3. Three were already in our investigation before the messages were sent.

---

### [The Circle Timeline — $515M Through Circle's Own System. $0 Frozen.](https://pifresearchlabs.github.io/drift-protocol-investigation/pif-circle-timeline.html)

The story nobody else is telling. Every dollar of stolen USDC was minted through Circle's own CCTP smart contracts. The first mint hit Ethereum at 10:40 AM ET — 86 minutes before the drain. Two minutes later, $10M was deposited to Binance. The attacker test-drove the getaway route through Circle's own infrastructure before pulling the trigger. After the exploit, stolen USDC sat on Ethereum for 7 hours. Circle had full visibility — it was happening inside their system. They froze $0. Over 50 hours, $515M flowed through 549 CCTP mints to attacker wallets. Tether froze $1.26B across 4,163 addresses in 2025. Circle froze $109M in all of 2023-2025. During this active, publicized exploit — they froze nothing. Full timeline with verified timestamps.

---

## Key Numbers (as of April 3, 2026)

| Metric | Value |
|--------|-------|
| Total extracted | $285M |
| Core drain time | 10 seconds |
| Drain rate | $23.3M per second |
| JLP vault drained | 99.9997% |
| Token types | 18 |
| Preparation time | 20 days |
| Rehearsal cost | < $1 (61 transactions) |
| Multisig timelock | 0 seconds |
| ETH vault | 130,262 ETH (~$278M) in 4 wallets, zero outbound |
| Binance deposits | $525M+ across 92 transactions |
| CCTP minted on Ethereum | $527M+ across 549 mints |
| Circle froze | $0 |
| First CCTP mint | 86 minutes before drain |
| First Binance deposit | 2 minutes after first mint |
| Solana dispersion bot | 364,000+ txns, 2,600+ wallets, 52+ hours |
| Chains active | 5+ (Solana, Ethereum, BSC, Base, CEXs) |

---

## How This Was Built

All data queried and verified directly from on-chain records. No third-party estimates. No assumptions. Every timestamp, every transaction hash, every wallet address pulled from the blockchain and cross-referenced.

---

## Contact

**PIF Research Labs** · [@PIFRESEARCHLABS](https://twitter.com/PIFRESEARCHLABS)

---

*Count When It's Quiet*
