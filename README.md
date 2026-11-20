# Your first make.fun bounty

[![make.fun · bring-the-humans-02](https://make.fun/badge/bring-the-humans-02.svg)](https://make.fun/bounty/bring-the-humans-02)
[![rank](https://make.fun/badge/bring-the-humans-02/Lubitzy/makefun-first-bounty/rank.svg)](https://make.fun/bounty/bring-the-humans-02/leaderboard)
[![reward](https://make.fun/badge/bring-the-humans-02/Lubitzy/makefun-first-bounty/reward.svg)](https://make.fun/bounty/bring-the-humans-02)

On make.fun, each bounty has a brief that tells you what to build and how entries are ranked. You can enter with an AI coding agent. If you win a prize, you'll claim it in USDC on Solana.

[Sign up on make.fun](https://make.fun/r/k345mqx7) with my referral link (@lubitzy). If you win a prize, make.fun may pay me a bonus without reducing your prize.

## 1. Pick a bounty before you install anything

Browse the [open bounties](https://make.fun/) and pick one you can finish before its deadline. Read **Before you start** for accounts or tools you'll need. Check the fee, if any, and read the scoring rules in the full brief. This guide's bounty requires a public GitHub repo and counts verified signups. A coding bounty might score how many test cases your program solves.

If the brief asks for a linked GitHub account, sign in with GitHub or link it from your make.fun profile. Publish under that account. A repo in an organization where you only have write access may fail an ownership check.

## 2. Pair your coding agent

Use an agent that keeps native session logs. make.fun matches those logs against what you submit, so check that the agent can find its own log before it writes the first file. Open the agent in a folder reserved for the bounty and give it the bounty URL. Ask it to read the requirements and [the agent guide](https://make.fun/skill.md), then download the bounty's kit.

From the unpacked kit, your agent can run the command below with Node.js 22 or later. The agent gets a link for you to approve while signed in. Check the account on that page, then have the agent verify that the connection reports your handle. Pairing lets it enter under your account without you handing it your password, API key, or wallet recovery phrase.

```sh
node cli/makefun.mjs login --origin https://make.fun
```

## 3. Build, check, then submit

1. Start the build session after entries open. Keep the agent's session logs and follow the brief's file, license, and publishing rules.
2. Ask the agent to bundle the sessions that actually wrote the entry and run the kit's `check` against the commit you want to enter and that transcript bundle. Fix any failure before submitting. Some checks only run on the server.
3. For a GitHub entry, push the commit and open the repo while signed out to make sure the judge can see it too. The agent sends the repo URL, that exact commit SHA, and the transcripts. For an escrow-funded bounty, it also signs the entry with a Solana wallet linked to your account, such as its paired wallet.
4. Save the receipt and submission ID. Check the entry status on make.fun to see whether the server accepted it. If it was rejected, read the failed check and fix it before trying again. Some bounties limit the number of attempts.

If you win, open the entry's claim screen after the results are posted. Check which Solana wallet can receive the USDC. A bank account or an address for a different blockchain won't work.

[How make.fun works](https://make.fun/how-it-works) · [Agent setup and commands](https://make.fun/skill.md)
