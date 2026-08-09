# Posting Friction & Flow on X — playbook

Two things about X that shape everything below:

1. **Link cards show only the image.** Since October 2023, X strips the headline and description from link previews and shows the image with a small domain label. Your `og:image` has to carry the message as text — which is why the preview card has the whole comparison baked into it.
2. **Posts with external links get less reach** than posts with native media. The card image counts as media, so a properly configured link post is fine — but a plain URL with no card performs badly.

---

## Step 1 — Publish to GitHub Pages

Upload **two files, both in the root of the repo** `FrictionFlowGame`:

- `index.html` — the game (named this so it loads at the bare URL)
- `og-card.png` — the preview image X will show

Both URLs are already baked into `index.html`, so the repo must stay named exactly `FrictionFlowGame` and the image must keep the name `og-card.png`.

1. Open your **FrictionFlowGame** repo. Confirm it is set to **Public** — Pages won't serve a private repo on a free account.
2. Click **Add file → Upload files**. Drag in both files. Click *Commit changes*.
3. Go to **Settings → Pages**. Under *Source* pick **Deploy from a branch**, branch **main**, folder **/ (root)**. Save.
4. Wait 1–3 minutes, then open your live URL:

```
https://scottrogers-az.github.io/FrictionFlowGame/
```

## Step 2 — Nothing to edit

The meta tags are already filled in with your username. Don't rename the repo or the PNG — that's what would break the preview card.

Confirm the image loads on its own first, before anything else:

```
https://scottrogers-az.github.io/FrictionFlowGame/og-card.png
```

If that shows the dark card, the preview will work.

## Step 3 — Check the card before you post

X retired its own Card Validator, so use a third-party preview tool — search "open graph preview" and paste your URL in. Confirm you see the dark card with the two comparison boxes.

> **The one mistake that's hard to undo:** X caches a card the first time it sees a URL. If you post before the image is live, the broken card sticks even after you fix it. If that happens, post the URL with `?v=2` on the end to force a fresh fetch.

---

## Post options

All are under 280 characters. Pick one — don't post several at once.

### A. The hook *(recommended)*

> $200,000 has to sit in a foreign bank account before anyone sends a single dollar.
>
> That's the part of cross-border payments nobody puts on a fee schedule.
>
> So I built a browser game about it. Free, no signup, ~10 minutes.

### B. The counter-intuitive one

> Everyone argues about the 6% fee.
>
> The number that actually decides the business is the $200,000 you park overseas per corridor — before a single customer walks in.
>
> Free browser game. Most people lose their first one chasing the fee.

### C. The challenge

> You run a money-transfer business. A bank is your competitor.
>
> Every payment: correspondent banking, or the XRP Ledger. Both costs shown in full, including the ones that aren't fees.
>
> First to deliver $1M wins. Free, plays in your browser.

### D. For teachers and explainers

> I couldn't find a good way to explain cross-border payments without a whiteboard, so I made a board game you play in a browser.
>
> Nostro accounts, trapped liquidity, settlement finality — all of it playable. Built-in teaching guide. Free, one file.

**Add to any of them:** the link on its own line at the end.

---

## The thread version

Threads outperform single link posts because each post earns its own impressions. Put the link in post 6, not post 1.

**1/**
> Sending $100,000 from the US to Mexico takes 2–5 days and costs about 6%.
>
> Everyone knows that part.
>
> Almost nobody knows why — and the real reason isn't the fee. 🧵

**2/**
> To pay someone in Mexico, your bank must already have money sitting in a Mexican bank account.
>
> Not when the customer shows up. Before.
>
> It's called a nostro account. And it has to be funded whether anyone sends money that day or not.

**3/**
> Now multiply that.
>
> 40 corridors means 40 accounts, each pre-funded, each doing nothing until someone needs it.
>
> That capital is on the balance sheet and unusable. The industry calls it trapped liquidity.

**4/**
> This is why banks quietly exit corridors that "aren't worth it," and why some countries lose banking access entirely.
>
> It's called de-risking. The fee was never the binding constraint. The parked capital was.

**5/**
> If a payment settles in seconds instead of days, you don't need to park anything. You source the destination currency at the moment of the payment.
>
> That's the actual argument for a bridge asset. Not speed for its own sake — capital that stops sitting still.

**6/**
> I built a free browser game so you can feel this instead of reading it.
>
> You run a payments business against a bank. Every payment, you pick a rail. It shows you both costs in full — including the case *against*.
>
> [your link]

---

## Things to avoid

- **Don't lead with price.** Price talk pulls in a crowd that won't play a teaching game and buries the actual idea.
- **Don't over-hashtag.** One at most, if any. `#XRP` will pull volume but a lot of it is low-quality engagement.
- **Don't oversell.** The game itself argues both sides — the endgame screen makes the case for incumbent rails. Say that in replies when someone pushes back. It's your strongest credibility move and it's already built in.
- **Don't post and vanish.** The first 30 minutes of replies drive distribution more than anything else.

## After posting

- **Pin it** to your profile. This has a long tail — it stays useful indefinitely.
- **Reply to your own post** with the sources: World Bank Remittance Prices Worldwide, and xrpl.org. Skeptics ask, and having it ready converts them.
- **Post the card image natively** in a follow-up a week later, with the link in a reply. Native images reach further than link cards, so the same asset gets you two bites.
