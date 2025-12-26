# Procedural World Generation
This is a simple boid ecosystem simulation inspired by Daniel Shiffman's (TheCodingTrain) Ecosystem simulation using the buy and sell pressure of a solana memecoin. 

![screenshot](/screenshot.png)

# Solana Memecoin Buy/Sell Pressure Simulator (Ecosystem)

A visual simulation that **turns memecoin market dynamics into an ecosystem**:

- **Buy pressure** creates “support” (growth + survival)
- **Sell pressure** creates “stress” (decline + extinction events)
- If **sell pressure outweighs buy pressure**, “predators” begin eliminating normal entities (capitulation-style behavior) :contentReference[oaicite:1]{index=1}
---

## What this is (and what it isn’t)

### ✅ What it is
A **market simulator** designed to help you *feel* and *see* how buy/sell imbalance can cascade through a system — similar to what happens in fast-moving Solana memecoins when volume shifts, liquidity thins, or sentiment flips.

### ❌ What it isn’t
- Not a real exchange, not on-chain execution, not a price oracle
- Not financial advice
- Not a prediction engine

Think of it like: **“market psychology as a nature documentary.”**

---

## The core idea

This sim models a memecoin chart as an environment with two major forces:

### 1) Buy Pressure (Demand / Bids / Support)
Buy pressure represents:
- new buyers entering
- existing holders adding
- strong bid support / momentum
- “green candles” behavior

In the ecosystem:
- buy pressure increases survivability and growth
- entities thrive and reproduce / persist longer (depending on your parameters)

### 2) Sell Pressure (Supply / Dumps / Exhaustion)
Sell pressure represents:
- profit-taking
- panic selling
- large holders distributing
- liquidity getting drained

In the ecosystem:
- when sell pressure dominates, the environment becomes hostile
- predators become more effective and normal entities get wiped out faster :contentReference[oaicite:3]{index=3}

---

## Mapping: memecoin market → ecosystem

Here’s the mental model this repo is aiming for:

| Memecoin concept | In the sim |
|---|---|
| Retail buyers, momentum traders | “Normal” entities (boids) |
| Aggressive sellers / distribution | Predators |
| Buy volume / bid strength | Buy pressure |
| Sell volume / ask pressure | Sell pressure |
| Capitulation | Predator wipeouts accelerate |
| Recovery / reversal | Buy pressure stabilizes population |

This makes it easier to explain *why* charts can “fall off a cliff” when selling overwhelms buying: once the system tips, negative feedback loops kick in.

---

## How the simulation behaves (high-level)

Each tick/frame:
1. The sim updates **buy pressure vs sell pressure** (based on your config and/or internal settings).
2. Entities move + behave according to the ecosystem rules.
3. Predators hunt more effectively when conditions favor sell pressure.
4. Graphs track what’s happening so you can correlate “pressure” with “population outcomes.”

If you want: you can treat “population size” as a proxy for:
- number of participants still active
- strength of community participation
- how “alive” the coin feels after volatility

--

## Configurations
- The project config file is located at `src/configs.rs`
