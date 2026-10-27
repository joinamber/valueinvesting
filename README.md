# The Arts of Value Investing

A personal thought pad on value investing, published at **[amberliang.xyz/valueinvesting](https://www.amberliang.xyz/valueinvesting)**.

## Goal

Share how I invest, in public and honestly. I bought my first stock at 25, chased trends, and lost five figures in 2022. After studying Munger, Buffett and Burry I built a framework of my own. This page is where that framework lives: the principles behind it, the small tools I built to practise it, the research that backs it, and a running scorecard of how it performs.

It is meant to read like a notebook, not a fund pitch. Losses come first, numbers are shown against a benchmark, and anything estimated is labelled as an estimate.

## Sections

The landing page ([`index.html`](index.html)) has four sections, in this order:

| # | Section | What it covers |
|---|---|---|
| 01 | **Philosophy** | The origin story, then three principles: the power of compounding, investing in durable businesses, and thinking like an owner. Two principles link to the matching tool. |
| 02 | **Vibe-coded toolkit** | Small tools built with AI to practise the framework: [The magic of compounding](https://compounding-simulator.vercel.app/), [Valuation Copilot](https://valuation-copilot.vercel.app/) and [What's your investor persona](https://investorpersona.vercel.app/). |
| 03 | **Research** | An index of research notes. It currently holds one report, *The opportunity cost of not investing*, marked as AI-assisted. |
| 04 | **Track record** | One card per year, showing return against the S&P 500. Year 1 is 2026 YTD; Year 2 (2027) is a placeholder. |

### Research articles

Each research note is a standalone page under [`research/`](research/):

- [`opportunity-cost-of-not-investing.html`](research/opportunity-cost-of-not-investing.html): saving and investment patterns in the top 50 economies, and what holding surplus cash costs young households. Created with AI as a research assistant. Its household and market-size figures are order-of-magnitude estimates, not forecasts.

### Track record

- Figures are percentages only, never dollar amounts.
- The benchmark is the S&P 500 total return, including dividends.
- Portfolio figures come from my own records. Benchmark figures are sourced from public data, and an estimate is labelled as such, with its date.
- To add a year, add a card to the `.years` grid in `index.html` and update the "as of" note beneath it.

## How it's built

- **Plain static HTML and CSS.** There is no framework and no build step.
- **Editorial look:** warm paper tones, Newsreader for text and IBM Plex Mono for labels and numbers, with a dark theme that follows the system setting.
- **Layout:** works down to phone width, with no horizontal scroll.

## Structure

```
index.html                                   Landing page (all four sections)
research/
  opportunity-cost-of-not-investing.html     Research article
vercel.json                                  Clean URLs and /valueinvesting path handling
LICENSE
```

## Running locally

```bash
python3 -m http.server 4326
```

Then open <http://localhost:4326>.

## Hosting

- This repo is its own Vercel project, **`valueinvesting`**. Every push to `main` deploys to production at [valueinvesting-pi.vercel.app](https://valueinvesting-pi.vercel.app/valueinvesting).
- The main site, [amberliang.xyz](https://www.amberliang.xyz), forwards `/valueinvesting` and `/valueinvesting/*` to this project through rewrites in its own `vercel.json`. The page's links therefore start with `/valueinvesting/...`, so they work on both domains.
- It lives in a separate repo so the thought pad can grow into more pages and deploy independently of the main site.

## Disclaimer

Personal notes, not investment advice. Past performance does not guarantee future results.
