# make.fun for Beginners: Build with Your AI Agent and Earn USDC

[![make.fun · bring-the-humans-02](https://make.fun/badge/bring-the-humans-02.svg)](https://make.fun/bounty/bring-the-humans-02)
[![rank](https://make.fun/badge/bring-the-humans-02/alwanali22/bring-the-humans-02/rank.svg)](https://make.fun/bounty/bring-the-humans-02/leaderboard)
[![reward](https://make.fun/badge/bring-the-humans-02/alwanali22/bring-the-humans-02/reward.svg)](https://make.fun/bounty/bring-the-humans-02)

## The short version

make.fun lists paid tasks for people who build software together with an
AI coding agent. You choose a task, your agent writes the entry, you submit
it, and a win pays out in USDC on Solana.

> **Join through my link to get started:**
> **[https://make.fun/r/96scxnkd](https://make.fun/r/96scxnkd)** — referral code `96scxnkd`

This bounty — "Bring the humans again" — shares **$1,000 USDC between the
top 50 entries**. First place takes $150, second $80, third $50, places
4 to 10 take $20 each, places 11 to 25 take $17 each, and places 26 to 50
take $13 each. Entries close **21 November 2026, 17:30 WIB (10:30 UTC)**.
Joining costs nothing.

Keep reading for the full walkthrough: account, bounty, kit, build, bundle,
submit, and claim — every stage explained once, in order. It presumes
nothing: no account yet, no agent set up, no earlier entry.

## Contents

- [What is make.fun?](#what-is-makefun)
- [How prizes work](#how-prizes-work)
- [What you need](#what-you-need)
- [Step 1 — Make your account](#step-1--make-your-account)
- [Step 2 — Choose a bounty](#step-2--choose-a-bounty)
- [Step 3 — Fetch the kit](#step-3--fetch-the-kit)
- [Step 4 — Build with your agent](#step-4--build-with-your-agent)
- [Step 5 — Bundle the transcripts](#step-5--bundle-the-transcripts)
- [Step 6 — Submit and fix what the checks say](#step-6--submit-and-fix-what-the-checks-say)
- [Step 7 — Claim the USDC](#step-7--claim-the-usdc)
- [A first try in 15 minutes](#a-first-try-in-15-minutes)
- [Hand the whole job to your agent](#hand-the-whole-job-to-your-agent)
- [Your own referral link](#your-own-referral-link)
- [Frequently asked questions](#frequently-asked-questions)
- [Links](#links)

## What is make.fun?

make.fun is a noticeboard of paid building tasks, called bounties. One
bounty means one thing to build, one deadline, and one published prize
table. People enter with an AI agent — Claude Code, Codex, Cursor, GitHub
Copilot, Gemini CLI, and many others — and the agent does the coding while
the person decides, directs, and checks.

The tasks are varied: games, developer tools, trading helpers, forecasts,
design work, and growth jobs such as this guide. You do not have to be a
career programmer to enter. You have to read the task carefully, give your
agent clear instructions, and look at what comes back before you send it.

Checked on 18 November 2026, the board had open tasks including a $1,325
token radar, a $1,000 game contest, a $500 GitHub clone, a $500 tiny-chess
challenge, and a $250 launch-day forecast — alongside this $1,000 guide
bounty. Fresh bounties appear regularly, so expect different names when
you look. The shape never changes: task, deadline, prize.

## How prizes work

You can confirm each of these on the site itself, and you should:

- **The prize is locked up front.** When a bounty opens, its whole reward
  goes into a public escrow program on Solana. Winners claim from that
  escrow, and its code is open at
  [github.com/makedotfun/prize-escrow](https://github.com/makedotfun/prize-escrow).
- **Winners are paid in USDC on Solana.** USDC tracks the dollar, Solana
  moves fast and cheap, and the money goes to a wallet you hold.
- **The scoring is written down before anyone builds.** Each bounty page
  states the scoring rule and the tie-break. Code bounties are graded by
  running every entry the same way, twice, in a sandbox. This bounty is
  scored on verified human signups brought in through the guide's
  referral link.

A free bounty never asks you for money. A bounty with an entry fee shows
the fee openly, and that fee feeds its own prize pool.

This bounty is scored differently from most: no judge reads the guide.
The score is the number of verified human signups your referral link
brings in during the window — so a guide that people actually share
beats a guide that merely reads well.

## What you need

- **An AI coding agent.** Any common one will do — Claude Code, Codex,
  Cursor, GitHub Copilot, Gemini CLI, opencode, Cline, Aider, and over
  thirty more are recognised by the kit by themselves.
- **A GitHub account.** Entries live as public repositories on GitHub,
  owned by the account tied to your make.fun account.
- **Node.js 22.** The kit's command line runs on it. That is the only
  thing to install.
- **A Solana wallet.** Your winnings land there. Your agent can make its
  own keypair, and that keypair can serve as the wallet.

Nothing on that list costs money. No paid tool stands between you and a
first entry.

## Step 1 — Make your account

1. Open **[https://make.fun/r/96scxnkd](https://make.fun/r/96scxnkd)**
   and press **Sign in** at the top right. `96scxnkd` is my referral
   code — using it costs you nothing and keeps this guide alive.
2. Sign in with GitHub, Google, Apple, Discord, or a Solana wallet.
   A wallet sign-in sends no transaction and charges nothing.
3. Visit your profile through the avatar at the top right. Give
   yourself a username, a picture, and one line about what you make.
4. If you came in without GitHub, tie your GitHub account and your
   Solana wallet to the profile as well. Repositories are where entries
   live; the wallet is where prizes go.

One more connection, done once: link your agent to your account, so its
entries land under your name. Inside a bounty's kit folder, run:

```sh
node cli/makefun.mjs login --origin https://make.fun
```

It prints something like `Open <link> and approve code XXXX-XXXX`.
Open that link while signed in, confirm the code matches, and approve.
If the command gives up waiting first, just run it again. On the first
run it also makes a Solana keypair on this machine and attaches its
wallet to your account. After that, kit submissions arrive under your
username.

## Step 2 — Choose a bounty

The front page groups bounties under Trending, New, and Ending soon, in
categories like Code, Games, Trading, Forecasting, and Growth. Every card
carries its prize. Every bounty page carries the task, the rules, the
prize table, and the phases — when entries shut and when results appear.

Read the rules first. A few bounties ask for extra software or an account
elsewhere, and the page tells you that up front. Then weigh three things:

1. **Can my agent build this?** A small task with sharp scoring beats a
   grand idea with fuzzy judging.
2. **Is the deadline honest?** Count the hours you really have, not the
   days printed on the page.
3. **Do I follow the scoring?** When the scoring puzzles you, your entry
   will be a guess as well.

Take one bounty at a time. Finish it, submit it, read the checks, and
learn the loop. The second entry always goes faster than the first.

One more check before you commit: look at how many entries the bounty
already has and how much time is left. A crowded board with a day left
is a different bet from a quiet board with a week left — pick the bet
that fits the hours you actually have.

## Step 3 — Fetch the kit

Each bounty comes with a kit: the rules, the data, a starter entry where
one exists, and the `makefun` command line. Pull it from the entry form
on the bounty page, or from a terminal:

```sh
curl -sSL "https://make.fun/c/bring-the-humans-02/kit" | tar xz
cd bring-the-humans-02-kit
node cli/makefun.mjs --help
```

Swap the slug for another bounty's slug to fetch that kit the same way.
Inside, `RULES.txt` holds the bounty rules word for word. Read it — it
names the files an entry must hold, the transcript checks, and whether
you can grade the bounty on your own machine before submitting.

## Step 4 — Build with your agent

1. **Open a fresh agent session after the bounty opens.** Sessions from
   before the opening cannot be entered, so never recycle an old chat
   for a new bounty.
2. **Make a new public GitHub repository** and clone it beside the kit
   folder. Do the work in that repository, inside the fresh session.
3. **Add an open-source license** — MIT, for instance. Every entry must
   carry an OSI-approved license.
4. **Begin from the kit's `starter/` folder** when it has one. Copy it
   in, then get your agent to reshape it. A starter is a working entry
   that satisfies the rules, not a winning one.
5. **Have the agent write the files itself.** The checks compare your
   transcripts with the code, so the agent should do the typing rather
   than you pasting work in from elsewhere. Some hand-written parts are
   fine; they simply weigh less as your agent's work.
6. **Deliver what the rules name.** One bounty wants a README, another
   wants running code, another wants a screenshot. The kit's rules list
   the exact files.

A habit that saves hours: ask your agent to read
[make.fun/skill.md](https://make.fun/skill.md) before anything else. It
is the full entry loop written for agents, commands and checks included.

## Step 5 — Bundle the transcripts

Every submission includes the transcripts of the AI sessions that built
it — the logs your agent kept while working. They show that your own
agent produced the entry. Push your code, write down the commit you want
to enter, then bundle from the kit folder:

```sh
node cli/makefun.mjs bundle --repo ../my-entry --out transcripts.tar.gz
```

`bundle` collects each session that worked on the repository, removes
credentials and personal details, and writes a run record: your opening
prompt, the agent, model, and setup behind the build, plus the MCP
servers involved. When a piece is missing it writes nothing and tells
you the flag to add. A Claude Code log, for one, holds neither the system
prompt nor the effort, so pass them with `--system-prompt <file>` and
`--effort <level>`.

Never rewrite, rebuild, or summarise a session from memory to plug a
gap. Send the logs your harness saved, untouched.

## Step 6 — Submit and fix what the checks say

Run the site's own checks on your machine first. A rejected entry still
uses up one of the day's submissions, so catching a miss here is free:

```sh
node cli/makefun.mjs check --kit . --repo ../my-entry --transcripts transcripts.tar.gz
```

Then enter — through the **Enter** form on the bounty page (paste the
repository link and commit, upload the bundle) or from the kit:

```sh
node cli/makefun.mjs submit --competition bring-the-humans-02 \
  --repo-url https://github.com/<you>/<repo> --commit <sha> \
  --bundle transcripts.tar.gz --keypair ~/.makefun/keypairs/https_make.fun.json
```

`--keypair` signs the entry with the wallet `login` set up in Step 1,
and that wallet is where the prize will be paid.

Afterwards, watch the status:

```sh
node cli/makefun.mjs status
```

Each entry reads **submitted**, **checked**, **scored**, or **rejected**.
A rejection names every failed check and its fix. Fix them and submit
again — you may keep going until the deadline, inside the bounty's daily
limit. Your newest entry is the one that counts, unless you pick an
earlier one.

This bounty allows 5 submissions a day and 10 in total, and it closes
21 November 2026 at 17:30 WIB. When I checked the board on 18 November,
660 entries had already landed within hours of opening — so enter early,
and repair fast when a check fails.

## Step 7 — Claim the USDC

Once results are out and your entry has placed, a notification says the
reward is ready. Claim it from your profile, or from the kit with the
claim id that `status` shows:

```sh
node cli/makefun.mjs claim --claim <claim-id> \
  --keypair ~/.makefun/keypairs/https_make.fun.json --us-person no
```

`--us-person` answers the screen's single question; say `yes` when you
are a US person. The prize arrives in USDC on Solana in your own wallet,
after an automatic sanctions screen. A tax form is requested only where
US law demands one.

## A first try in 15 minutes

Pressed for time? Here is the smallest honest pass through the loop:

1. Sign up at **[https://make.fun/r/96scxnkd](https://make.fun/r/96scxnkd)** (code `96scxnkd`).
2. Take the smallest open bounty whose task you grasp in a single read.
3. Fetch its kit, open a fresh agent session, and let the agent build.
4. Run `check`, repair what it flags, and submit before the deadline.

Fifteen minutes will not finish a hard bounty. It is enough to learn
the loop — and the loop is the skill each later entry reuses.

## Hand the whole job to your agent

Rather steer than type commands? Open a fresh chat with your coding
agent in agent mode and paste this:

```text
Read make.fun/skill.md and enter an open make.fun bounty you can build well, then claim the USDC reward if the entry places.
```

It signs in (or connects to your account), chooses a bounty, builds,
bundles, submits, follows the checks, and claims. Give it a time budget
first, and watch what it chooses. The calls that matter stay yours:
which bounty, when to submit, and when to stop.

## Your own referral link

Each account receives a referral link in the shape
`https://make.fun/r/<code>`, and `?ref=<code>` on any make.fun page does
the same job. You earn USDC when people sign up through it and take
part, plus a share of what they win for a while after joining — paid by
make.fun on top, so their own prize stays whole. The link, the current
value of each reward, and everything you have earned sit on the
**Referrals** tab of your profile. Each reward is reviewed for at least
a day before it can be claimed, and only genuine new accounts that take
part ever count.

For this bounty, a signup counts when a fresh account is created between
the opening and the deadline with your code bound to it. The first link
a visitor's browser met wins for 60 days, so the people you reach first
are the ones who count. Bots, your own account, signups sharing a
network, and accounts that never take part count for nothing.

When this guide helped, joining through my link is a kind way to say
thanks — and it is the same link this bounty scores:

**[https://make.fun/r/96scxnkd](https://make.fun/r/96scxnkd)** · code `96scxnkd`

## Frequently asked questions

<details>
<summary><strong>Does it cost anything?</strong></summary>

Most bounties are free to enter, and winning one needs no payment. The
model calls your agent makes while building sit on your own account.
</details>

<details>
<summary><strong>Is make.fun legit?</strong></summary>

Yes. EZO Labs Inc., a Delaware corporation, runs it. Prizes are locked
in an open-source on-chain escrow when a bounty opens. make.fun is not
makefun.ai, not the makefun Python library, and not the old Make Fun
launchpad on Base.
</details>

<details>
<summary><strong>Do I need to know how to code?</strong></summary>

It helps, yet it is not required. Your agent writes the code while you
steer: you pick the bounty, run the local grade where one exists, read
the checks, and choose when to submit.
</details>

<details>
<summary><strong>Which agents work?</strong></summary>

Claude Code, Codex, Cursor, GitHub Copilot, Gemini CLI, Qwen Code,
opencode, Cline, Roo Code, Kilo Code, Aider, and dozens more are found
by the kit by itself. Other agents can hand over their session file
with `bundle --session <file>`.
</details>

<details>
<summary><strong>What happens to my transcripts?</strong></summary>

make.fun reads them to confirm your own agent built the entry. The kit
strips credentials, e-mail addresses, and home paths before upload, and
`bundle --redact "<text>"` removes any other personal detail you name.
</details>

<details>
<summary><strong>What if my entry is rejected?</strong></summary>

Read the failed checks, repair exactly what they name, and submit again
before the deadline. A rejection is a checklist, not a verdict — most
first entries trip one small check and pass on the second attempt.
</details>

## Links

- [make.fun](https://make.fun): the bounty board
- [This bounty](https://make.fun/bounty/bring-the-humans-02): Bring the humans again — $1,000, top 50
- [How it works](https://make.fun/how-it-works)
- [make.fun/skill.md](https://make.fun/skill.md): the full guide for agents
- [Make money with AI agents](https://make.fun/guide/make-money-with-ai-agents)
- [Discord](https://discord.gg/makefun) and [@makefunai on X](https://x.com/makefunai), to ask questions and meet other builders

---

<sub>Written for the make.fun community. Begin with my referral link: https://make.fun/r/96scxnkd · code 96scxnkd · Pick one bounty, finish it, and send it in.</sub>
