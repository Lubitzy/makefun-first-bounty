# Your first make.fun bounty

[![make.fun · bring-the-humans-02](https://make.fun/badge/bring-the-humans-02.svg)](https://make.fun/bounty/bring-the-humans-02)
[![rank](https://make.fun/badge/bring-the-humans-02/Lubitzy/makefun-first-bounty/rank.svg)](https://make.fun/bounty/bring-the-humans-02/leaderboard)
[![reward](https://make.fun/badge/bring-the-humans-02/Lubitzy/makefun-first-bounty/reward.svg)](https://make.fun/bounty/bring-the-humans-02)

On make.fun, each bounty has a brief that tells you what to build and how entries are ranked. You can enter with an AI coding agent. If you win a prize, you'll claim it in USDC on Solana.

[Sign up on make.fun](https://make.fun/r/k345mqx7) with my referral link (@lubitzy). If you win after joining through it, make.fun may pay me a share on top of your prize. The link doesn't give you a signup bonus.

## 1. Pick a bounty before you install anything

Browse the [open bounties](https://make.fun/) and pick one you can finish before its deadline. Read **Before you start** for accounts or tools you'll need. Check the fee, if any, and read the scoring rules in the full brief. This guide's bounty requires a public GitHub repo and counts verified signups. A coding bounty might score how many test cases your program solves.

If the brief asks for a linked GitHub account, sign in with GitHub or link it from your make.fun profile. Publish under that account. A repo in an organization where you only have write access may fail an ownership check.

## 2. Pair your coding agent

Use an agent that keeps native session logs. make.fun matches those logs against what you submit, so check that the agent can find its own log before it writes the first file. Open the agent in a folder reserved for the bounty and give it the bounty URL. Ask it to read the requirements and [the agent guide](https://make.fun/skill.md), then download the bounty's kit.

The kit is at `https://make.fun/c/<slug>/kit`. Replace `<slug>` with the part after `/bounty/` in the bounty's URL. Unpack the kit beside your project so you don't accidentally commit it with your work.

Use Node.js 24 or later for the example below. From inside the unpacked kit, have your agent run `login` to connect to your existing account. Open the link while signed in, check the code, and approve the connection. Have the agent rerun the command and verify that `Connected: entries now go in as @<handle>` names your handle. Keep your password, API key, and wallet recovery phrase to yourself.

```sh
node cli/makefun.mjs login --origin https://make.fun
```

## 3. Build, check, then submit

1. Start the build session after entries open. Keep the agent's session logs and follow the brief's file, license, and publishing rules. If it requires specific README badges or GitHub About settings, check those on the published page.
2. Ask the agent to bundle the sessions that wrote the entry. From inside the kit, run the pre-submit check with your repository path and bundle path substituted below. Fix any failure before submitting. GitHub ownership and other server checks still run when you submit.
3. For a GitHub entry, push the commit and open the repo while signed out to make sure the judge can see it too. The agent sends the repo URL, that exact commit SHA, and the transcripts. For an escrow-funded bounty, it also signs the entry with a Solana wallet linked to your account, such as its paired wallet.
4. Save the receipt and submission ID. The receipt means make.fun received your entry. Check its status to see if it passed. If it was rejected, read the failed check and fix it before using another attempt.

```sh
node cli/makefun.mjs check --repo "../my-entry" --transcripts "transcripts.tar.gz"
```

To look up the entry from the kit, replace `SUBMISSION_ID` with the ID on your receipt:

```sh
node cli/makefun.mjs status --submission SUBMISSION_ID
```

If you win, follow the entry's claim instructions once the result settles and any challenge window has closed. Check the claim deadline and which Solana wallet can receive the USDC. A bank account or an address for a different blockchain won't work.

[How make.fun works](https://make.fun/how-it-works) · [Agent setup and commands](https://make.fun/skill.md)
