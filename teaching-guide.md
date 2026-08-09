# Friction & Flow: The Liquidity Loop — Teaching Guide

A companion to `friction-and-flow.html`. Everything below explains what the game is doing under the hood and why each mechanic exists.

---

## The one-paragraph version

Most explanations of XRP start with the price. This game starts with the problem. You run a money-transfer business competing against a traditional bank. Every corridor space forces one decision — send this customer's money by correspondent banking, or bridge it over the XRP Ledger — and shows you the full cost of both, including the cost nobody puts on a fee schedule: the capital you have to park overseas before anyone even asks you to send anything.

---

## How to play

**Goal.** Deliver $1,000,000 of customer payments before Meridian Trust Bank does. Run your working capital below zero and you lose.

**Turn.** Roll, move around the 20-space loop, resolve the space you land on.

| Space | What it does |
|---|---|
| **Corridor** (8) | A customer payment of $40k–$120k arrives. Pick a rail. This is the game. |
| **Friction card** (4) | Cut-off times, frozen accounts, hidden FX spreads, de-risking, tracing fees. |
| **Flow card** (4) | Atomic settlement, path-finding, auto-bridging, 10-drop fees, instant finality. |
| **Ledger Close** (corner) | Pass or land on it: collect $25,000. |
| **Compliance Review** (corner) | Pay AML/KYC costs — on *both* rails. |
| **Market Open** (corner) | The XRP price moves. |
| **Capital Call** (corner) | Pay 2% carrying cost on everything parked overseas. |

---

## The two rails, and what each one really costs

### Correspondent banking

To pay someone in Mexico, you must already have money sitting in a Mexican bank account — a **nostro account**. Not when the customer shows up. Before. In the game that's $200,000 locked per corridor, and it never comes back until you close the account.

- Fees run 5.2%–7.7% depending on corridor, tracking the World Bank's regional averages
- Arrival takes 2–3 turns, standing in for 2–5 business days
- The account is drawn down while a payment is in flight, so you lose capacity in that corridor
- Friction cards can freeze it, close it, or delay everything in transit

Serve four corridors and $800,000 of your $500,000 starting capital is spoken for. You can't. That constraint *is* the lesson — in the playtests, the legacy-only strategy had to turn away roughly seven customers per game simply because it hadn't pre-funded the corridor they wanted.

### The XRP bridge (on-demand liquidity)

You take the customer's money, convert to XRP, send it, and convert to the destination currency on arrival. Nothing was parked in advance.

- **Network fee: 10 drops — 0.00001 XRP.** It isn't paid to a miner or a bank. It's destroyed, purely to make spam expensive
- **Settles in 3–5 seconds**, which is one turn on this board — and continuously, including weekends and holidays
- **Nothing pre-funded.** Zero trapped capital
- **But:** you're pricing through a live market, so a large payment on a thin pair costs you slippage. The game charges 0.05%–0.6%, scaling with size

---

## The honest counterweight

The board is deliberately not a sales pitch. Three things cut the other way, and the game says so at the end of every match:

1. **Correspondent banking moves the overwhelming majority of the world's cross-border value today.** It's embedded in law, contracts, compliance infrastructure and habit. Incumbency is a real advantage, not a rounding error.
2. **Bridging depends on market depth at both ends.** Slippage is not a token mechanic — it's the genuine limit on very large bridged payments, and it's why the corridor matters as much as the technology.
3. **Compliance doesn't go away.** The Compliance Review corner charges both players. Faster settlement changes the plumbing, not the obligation.

A player who finishes the game thinking "XRP is free" has misread it. The point is narrower and more defensible: *the pre-funding requirement is the expensive part of the old model, and settling in seconds is what removes it.*

---

## Concepts the game teaches, and where they appear

| Concept | Where you meet it |
|---|---|
| Nostro / vostro accounts | Every corridor space |
| Trapped liquidity | Pre-funding a corridor; the Trapped Capital counter |
| Correspondent chain | Middleman Tax card |
| Banking hours / cut-offs | Cut-Off Time and Weekend & Holiday cards |
| 24/7/365 settlement | The contrast to those same cards |
| De-risking | De-Risking card |
| FX spread | FX Spread Squeeze card |
| Failed payments | Wrong SWIFT Code card |
| Cost of capital | Capital Call corner, Idle Float card |
| Atomic settlement | Atomic Settlement card |
| Path-finding | Path-Finding card |
| Auto-bridging | Auto-Bridging card |
| Consensus (no mining) | Consensus card |
| Ledger close | Passing Start; The Ledger Closes card |
| Transaction cost (10 drops) | Ten Drops card; every XRP send |
| On-demand liquidity | Capital Freed card; every XRP send |
| Finality | Deterministic Finality card |
| Slippage | Market Open corner; large XRP payments |

The sidebar tracks these as locked/unlocked, so a player can see how much of the map they've actually walked. Typical game unlocks 15–16 of 18.

---

## Discussion questions

Good for a classroom, a workshop, or a debrief after a match.

1. You lost $6,500 in fees on a $100,000 payment, and separately you have $200,000 sitting idle in a foreign account. Which one costs your business more over a year? Show your working.
2. Why would a bank keep using a rail it knows is slower and more expensive?
3. The 10-drop fee is destroyed rather than paid to anyone. Why design it that way instead of paying it to validators?
4. De-risking closed your corridor and handed your capital back. Was that good or bad for you? What about for the people who live in that country?
5. Where does slippage stop being a rounding error and start being the deciding factor?

---

## Where the numbers come from

**Corridor fees** track the World Bank's *Remittance Prices Worldwide* dataset — a 6.49% global average as of 2025, against a UN target of 3%. Sub-Saharan Africa runs around 7.7%, South Asia around 5.2%. Banks as a provider class average roughly 15%, well above money transfer operators.

**XRP Ledger figures** come from xrpl.org: a minimum transaction cost of 10 drops (0.00001 XRP), destroyed rather than paid to a validator; ledgers validating every 3–5 seconds under normal conditions; and a consensus protocol with no mining or proof-of-work.

**Simplified for playability:** the $200,000 pre-funding figure. Real nostro balances vary enormously by corridor and institution — this is a representative number, not a quoted one. Settlement "days" are compressed into turns.

---

## Running it

Open `friction-and-flow.html` in any browser. No installation, no internet connection, no accounts. One file — you can email it, put it on a USB stick, or host it anywhere.

Tested across 36 full simulated games: no errors, average game length 24–32 turns, and no strategy wins every time. XRP-heavy play wins roughly 60–75% of matches, which is the intended shape — a clear lesson that still has to be played for.
