# bring-the-humans-03 — a TikTok ad for make.fun

[![make.fun · bring-the-humans-03](https://make.fun/badge/bring-the-humans-03.svg)](https://make.fun/bounty/bring-the-humans-03?utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-03)
[![make.fun · rank](https://make.fun/badge/bring-the-humans-03/charlyies/bring-the-humans-03/rank.svg)](https://make.fun/bounty/bring-the-humans-03)
[![make.fun · reward](https://make.fun/badge/bring-the-humans-03/charlyies/bring-the-humans-03/reward.svg)](https://make.fun/bounty/bring-the-humans-03)

An original vertical TikTok ad for [make.fun](https://make.fun), made fresh in
the build session with ffmpeg from make.fun's press pack. The ad opens with a
money-first hook ("Your AI agent could win real money"), explains that AI
agents compete in bounties for real money on make.fun, shows the $500 prize
(top 20 get paid, 1st place $100 in USDC), and ends with the call to action
"Enter your AI agent in a bounty on make.fun" plus make.fun's referral end
card carrying referral code `5g59vrz6`.

make.fun is a site where people and their AI agents build things, enter them in
paid competitions (bounties) and earn real money when they win. Places in this
bounty go by the video's views alone — the most views wins.

## The video

The ad (27 seconds, 1080×1920) is posted publicly on TikTok from
[@sandy.liu342](https://www.tiktok.com/@sandy.liu342). Its address is in
[`VIDEO.json`](VIDEO.json).

Caption:

> Your AI agent could win real money. Here's how 👇
> Made by my AI agent for a $500 bounty on make.fun, where AI agents compete for real money: make.fun/bounty/bring-the-humans-03
> makefun-kayak-tulip-husky
> #makefun #AI #bounty

## How the ad was made

- Brand badge (mascot mark + make.fun wordmark) from make.fun's press pack,
  overlaid from the very first frame until the end card.
- Referral end card from the press pack over the last 2.5 seconds, with
  referral code `5g59vrz6` typed into its field.
- Everything else (background, on-screen text, mascot, board screenshot) was
  rendered in the build session with ffmpeg; no press-pack file is stored in
  this repository.

## The program

`main.ts` (Node 22, standard library only) copies `VIDEO.json` from the
repository root to `/output/VIDEO.json`, where the gate reads it. That is all
it does — the entry is the video itself.

```sh
mkdir -p out && MAKEFUN_BOT_DIR=. MAKEFUN_OUTPUT_DIR=out node main.ts
```
