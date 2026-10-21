# Agentic Engineering 101: AI Coding Tools for Students

A guide to AI coding agents for university students who get ridiculous amounts of free compute, credits, and trials. Seriously, use the hell out of the student perks while you still have them. These companies are lighting money on fire to win users. You might as well stand near the fire.

> Last reviewed: July 13, 2026. Pricing, quotas, models, and student offers change constantly. The numbers below are approximate on purpose. Approximate does not mean useless.

## Quick Reference

| Tool | What you actually get | Best for | Student perk |
|------|------------------------|----------|--------------|
| **OpenAI Codex** | **Plus $20:** roughly **$700/month** API-retail equivalent at the ceiling. **Pro 5x $100:** roughly **$3,500/month**. **Pro 20x $200:** up to roughly **$14,000/month** ([new 20x sign-ups paused since Sep 10, 2026](https://help.openai.com/en/articles/9793128)). | Best overall. Long tasks, repo-wide work, parallel agents, worktrees, PRs. | [Eligible US and Canadian university students get $100 in ChatGPT credits for Codex](https://developers.openai.com/community/students) |
| **Claude Code** | **Pro $20:** roughly **$400/month** API-retail equivalent. **Max 5x $100:** roughly **$2,000/month**. **Max 20x $200:** up to roughly **$8,000/month**. Limits reset every five hours, with weekly and monthly caps possible. | Precise edits, planning, front-end work, taste. | Mostly institution-wide through [Claude for Education](https://claude.com/solutions/education), not a universal individual discount |
| **GitHub Copilot** | Free gives 2,000 completions/month. Pro $10 includes **$15** in monthly AI credits, Pro+ $39 includes **$70**, Max $100 includes **$200**. | IDE integration, autocomplete, boring reliability. | [Copilot Student is free for verified students](https://github.com/education/students). Auto model selection only, no third-party agents. |
| **Cursor** | Free tier, then Pro starts at $20/month with a bundled model-usage bucket and metered overage. Cursor does not publish a clean API-dollar equivalent anymore. | Fast editor-first experiments and quick changes. | The blanket free year is dead. Current student discounts are event promotions through [Cursor Students](https://cursor.com/students) |
| **OpenCode** | The app is open source. Use free models or plug in whatever provider is cheapest this week. | Best open, provider-flexible terminal UX. Parallel sessions are excellent. | Free to install |
| **Gemini CLI** | Free tier ended June 18, 2026. Free users were moved to Antigravity CLI. | Only worth it with a paid Gemini API key. | None |
| **Google Antigravity** | Plan-dependent limits. Google AI plans expand them, but Google still does not publish a useful universal dollar equivalent. | Planning and agent-first IDE experiments. | Often bundled into Google AI plans |
| **Google AI Studio** | Free access varies by model and region, and the limits are still difficult to hit for ordinary prototyping. | Prompting, model testing, one-off prototypes. | Free tier |
| **Perplexity Education Pro** | Discounted Pro access for verified students and educators. | Research, source discovery, and getting unstuck before coding. | [Education Pro](https://www.perplexity.ai/help-center/en/articles/12590157-what-is-education-pro) |

### What “API-retail equivalent” means

It means: if you bought the same token volume through the public API, what would the retail bill look like?

It does **not** mean OpenAI or Anthropic literally spent that much serving you. API prices include margin. It is still the only sane common unit for comparing subscriptions that hide their real token allowances behind “5x usage,” rolling windows, and vibes.

[SemiAnalysis bought every OpenAI and Anthropic subscription tier](https://x.com/SemiAnalysis_/status/2064815044085318040), ran long-horizon coding tasks until the weekly limits were dead, then converted the consumed tokens to API retail prices. Their measured ceilings were roughly **$14,000/month for ChatGPT Pro 20x** and **$8,000/month for Claude Max 20x**. [Tom's Guide](https://www.tomsguide.com/ai/the-math-doesnt-work-why-your-usd200-ai-subscription-is-secretly-worth-thousands) and [Tom's Hardware](https://www.tomshardware.com/tech-industry/artificial-intelligence/ai-costs-spike-as-subscriptions-hit-pricing-wall-firms-turn-towards-chinese-llms-open-source-models-to-extend-budget) both reported the methodology and results.

The lower-tier estimates in this guide are simple linear approximations from those measured 20x ceilings and the providers' official 1x, 5x, and 20x ratios:

| Plan | Subscription price | Rough API-retail ceiling | Retail value / price |
|------|--------------------|---------------------------|----------------------|
| ChatGPT Plus | $20/month | ~$700/month | ~35x |
| ChatGPT Pro 5x | $100/month | ~$3,500/month | ~35x |
| ChatGPT Pro 20x | $200/month | ~$14,000/month measured by SemiAnalysis | ~70x |
| Claude Pro | $20/month | ~$400/month | ~20x |
| Claude Max 5x | $100/month | ~$2,000/month | ~20x |
| Claude Max 20x | $200/month | ~$8,000/month measured by SemiAnalysis | ~40x |

Real usage is not perfectly linear. Model choice, caching, task length, hidden reasoning, tool calls, and provider throttling all matter. Use the number. Do not worship the number.

## Tier 1: Worth Paying For

### [OpenAI Codex](https://openai.com/codex/)

This is still the best overall coding agent. Not “one of the best.” The best.

Codex is strongest when the task is bigger than one file: understanding a repository, planning a change, editing across the codebase, running tests, opening pull requests, working in separate worktrees, and delegating independent work to subagents. It is the tool I trust most to take a real engineering task from “here is the problem” to “here is the verified diff.”

The limits are also ridiculous. OpenAI officially sells Plus at $20, Pro 5x at $100, and Pro 20x at $200. SemiAnalysis managed to push the 20x tier to roughly $14,000 of API-equivalent token usage in a month. Even if your workload only extracts a fraction of that, the subscription economics are completely insane.

The weak spot is still front-end taste. Codex can build the UI, but it gets sloppy when the visual details matter. For polished front-end work, I still prefer Claude, then I verify the result in a real browser instead of trusting a screenshot and a victory speech.

The student deal is real: verified university students in the US and Canada can claim **$100 in ChatGPT credits for Codex**. These are not API credits. They extend Codex usage in ChatGPT and expire 12 months after the grant date.

### [Claude Code](https://claude.com/product/claude-code)

Claude Code is still really, really good. Its planning is excellent, its edits are precise, and it has better visual taste than Codex. When I care about front-end polish or I want a careful surgical change instead of an agent bulldozing through the repository, Claude is usually my second tool.

The annoying part is the meter. Claude Pro resets every five hours and Anthropic says a light chat workload gets around 45 short messages per window. Max 5x gets at least 225, and Max 20x gets at least 900. Those are chat-style estimates, not coding sessions. Claude Code burns through context, tool calls, and hidden work much faster, so do not look at “900 messages” and imagine 900 giant repo tasks.

The subscription is still an absurd deal. SemiAnalysis measured the $200 Max 20x ceiling at roughly $8,000/month in API-retail usage. The rough linear equivalents are about $400 for Pro and $2,000 for Max 5x.

There is no universal individual student discount. The real education route is [Claude for Education](https://claude.com/solutions/education), which is sold to universities. If your school has it, great. If not, yelling “but I am a student” at the pricing page does nothing.

### [Cursor](https://cursor.com/)

Cursor is still great for random vibe-coding experiments and fast editor changes. The UX is polished, Tab is useful, and sometimes you just want to stay inside a VS Code-shaped thing instead of living in a terminal.

It is not my main tool anymore. The old automatic one-year-free student deal is gone, and Cursor's current pricing is deliberately less clean than the old “you get about this much API credit” model. Pro starts at $20, each tier includes a model-usage bucket, and overage is billed after that. Cursor itself recommends Pro+ for daily agent use and Ultra for power users.

So the honest summary is simple: start free, pay if the editor workflow clicks for you, and watch the usage meter. Do not pretend the current student page is still the old deal. It is not.

## Tier 2: Ridiculous Value Because It Is Free or Subsidized

### [GitHub Copilot](https://github.com/features/copilot)

Copilot is boring in the best possible way. It is everywhere, it integrates with the IDE, and verified students get it free.

The current consumer plans are also unusually transparent: Pro costs $10 and includes $15 in monthly AI credits, Pro+ costs $39 and includes $70, and Max costs $100 and includes $200. The free plan gives 2,000 completions per month. GitHub finally put actual dollar-denominated usage numbers on the page instead of making everyone reverse-engineer “premium request multipliers.” Good.

Would I choose Copilot over Codex for serious autonomous work? No. Would I install it for free as a student? Obviously. Not doing that is just leaving value on the table for no reason.

### [Gemini CLI](https://github.com/google-gemini/gemini-cli)

This used to be the best free backup: 1,000 requests a day on a personal Google account. That's over. [Google stopped serving free Gemini CLI users on June 18, 2026](https://developers.googleblog.com/an-important-update-transitioning-gemini-cli-to-antigravity-cli/) and pointed everyone at Antigravity CLI. Gemini CLI still works with a paid API key.

[Antigravity's free plan](https://antigravity.google/pricing) has "basic weekly rate limits," and early users [report hitting them fast](https://www.theregister.com/ai-ml/2026/05/20/bye-bye-gemini-cli-google-nudges-devs-toward-antigravity/5243605). Try it, but don't plan around it.

### [OpenCode](https://opencode.ai/)

OpenCode has one of the best terminal interfaces in the category. It feels a lot like Claude Code, supports LSP, runs multiple sessions in parallel, and lets you connect different providers instead of marrying one company forever.

The app is free and open source. Model usage depends on what you connect. Use the free models for disposable work, then route hard tasks to a stronger provider when the cheap model starts hallucinating its way through the type system.

## Tier 3: Useful, But Not My Main Coding Agent

### [Google Antigravity](https://antigravity.google/)

Antigravity is Google's agent-first development environment. It is decent for planning and experiments. The UX is not good enough for me to live in it, and the public limits are too plan-dependent to pretend there is one clean dollar figure.

Use it when it is bundled into something you already pay for. Do not buy an entire Google plan just because one marketing page says “agentic.”

### [Google AI Studio](https://aistudio.google.com/)

AI Studio is excellent for testing prompts, comparing models, playing with long context, and building quick API prototypes. It is not a replacement for a repository-aware coding agent.

The free usage can be enormous depending on the model and region. Treat it as a lab bench, not your main workshop.

### [Perplexity Education Pro](https://www.perplexity.ai/help-center/en/articles/12590157-what-is-education-pro)

Perplexity is not my coding agent. It is my “find the source, compare the docs, and stop guessing” tool.

The old free-year student deal is gone. The current offer is Education Pro, a discounted plan for verified students and educators. Still useful, just not the lottery ticket it used to be.

Here is my [Perplexity referral link](https://plex.it/referrals/8N3ELADE) if you want to help me out.

## Pro Tips

### Put Instructions in the Repository

Stop pasting a giant system prompt into every new session. Put an `AGENTS.md` in the repository. Codex, Copilot, Cursor, and OpenCode read it, and [Claude Code reads it too when there's no `CLAUDE.md`](https://code.claude.com/docs/en/memory#agents-md) (since September 2026). One file, every tool.

Keep it short. It loads every session, and a bloated file gets ignored. Put in what the agent can't figure out by reading the code: setup and test commands, non-obvious conventions, dangerous areas, and what "done" means. Skip folder tours and generic advice. When the agent keeps making the same mistake, add a line. When a line stops mattering, delete it.

If something must happen every single time (formatting, blocking edits to a folder), use a hook instead. Instructions are advice. Hooks are enforced.

### Use LSP

LSP stands for Language Server Protocol. It gives the agent real-time information about type errors, missing imports, symbols, and syntax.

Turn it on. An agent with LSP can catch mistakes while writing. An agent without it is guessing, running the build, failing, and acting surprised.

### Use Skills and Subagents

Skills are reusable workflows that load only when relevant. Subagents are fresh workers for narrow jobs, with their own context so the main session stays clean.

A skill is just a folder with a `SKILL.md`. It's an [open standard](https://agentskills.io/specification), so the same skill works in Codex (`.agents/skills/`), Claude Code (`.claude/skills/`), Copilot, and most other agents. Write it once.

Use them for independent research, implementation, tests, review, migrations, or separate bug fixes. Do not spawn eight agents into the same branch and call it orchestration. That is just a race condition with a chat interface.

Useful starting points:

- [Codex skills](https://learn.chatgpt.com/docs/build-skills)
- [Codex subagents](https://learn.chatgpt.com/docs/agent-configuration/subagents)
- [Claude Code skills](https://code.claude.com/docs/en/skills)
- [Claude Code subagents](https://code.claude.com/docs/en/sub-agents)

### Use One Branch or Worktree per Task

Parallel agents are only useful if they stop stepping on each other.

Give every independent task its own branch or worktree. Keep the scope small. Review through pull requests. Merge after the tests pass. This is not glamorous, but neither is recovering three agents' half-overwritten changes from one dirty working tree.

### Require Verification

“Done” is not evidence.

Make the agent run the tests, linter, type checker, build, and browser checks that matter. Make it report the actual output. Read the diff. Agents are very good at sounding finished five minutes before they are finished.

### Use Agent Apps for Multi-Tasking

If you have twelve terminal windows open like a maniac, use an app that can manage parallel sessions cleanly. The Codex app and T3 Code are interfaces around the agents, not magical new model providers, but the interface matters when you are juggling real work.

### Use Voice Dictation

[Wispr Flow](https://wisprflow.ai) is still excellent for talking through code, file names, and structured instructions without typing everything. Here is my [referral link](https://wisprflow.ai/r?ARIO16).

### Check the Data Policy

Free compute is not charity.

Before feeding a tool private coursework, unpublished research, credentials, client data, or company code, read the current data-use settings. Turn on privacy mode where it exists. Keep secrets out of prompts. “But the model needed my production token” is not a security strategy.

## My Durable Setup: [Compass](https://github.com/ariobarin/compass)

Want the actual setup behind this guide instead of another folder full of random prompts? Use **Compass**.

Compass is my reviewed, portable agent setup. It contains the instructions, agents, skills, workflows, install wiring, and verification scripts I use across Codex and related tools. It is opinionated because generic configuration is usually useless configuration.

## My Workflow

| Situation | Tool |
|-----------|------|
| Most coding tasks | **OpenAI Codex** |
| Starting from scratch and planning carefully | **Codex** or **Claude Code** |
| Quick, precise edits | **Claude Code** |
| Front-end work that needs to actually look good | **Claude Code**, then verify in a browser |
| Random vibe-coding experiments | **Cursor** |
| IDE autocomplete that costs students nothing | **GitHub Copilot** |
| Open or provider-flexible terminal workflow | **OpenCode** |
| Free backup when subscriptions run dry | **OpenCode** with a free model |
| Research and source discovery | **Perplexity** |
| Durable instructions, skills, and workflows | **Compass** |

The exact model matters less than the engineering loop around it: give the agent real context, isolate the work, make it verify the result, review the diff, and stop accepting confident nonsense as evidence.

## Sources

### Usage economics

- [SemiAnalysis subscription stress test](https://x.com/SemiAnalysis_/status/2064815044085318040)
- [Tom's Guide summary of the SemiAnalysis results](https://www.tomsguide.com/ai/the-math-doesnt-work-why-your-usd200-ai-subscription-is-secretly-worth-thousands)
- [Tom's Hardware summary of the SemiAnalysis results](https://www.tomshardware.com/tech-industry/artificial-intelligence/ai-costs-spike-as-subscriptions-hit-pricing-wall-firms-turn-towards-chinese-llms-open-source-models-to-extend-budget)

### Official pricing and limits

- [ChatGPT pricing](https://chatgpt.com/pricing/)
- [ChatGPT Pro 5x and 20x tiers](https://help.openai.com/en/articles/9793128)
- [Codex for Students](https://developers.openai.com/community/students)
- [Claude pricing](https://claude.com/pricing)
- [Claude Pro usage limits](https://support.claude.com/en/articles/8324991-about-claude-s-pro-plan-usage)
- [Claude Max usage limits](https://support.claude.com/en/articles/11014257-about-claude-s-max-plan-usage)
- [GitHub Copilot pricing](https://github.com/features/copilot/plans)
- [GitHub Education for students](https://github.com/education/students)
- [Cursor pricing](https://cursor.com/pricing)
- [Cursor for Students](https://cursor.com/students)
- [Gemini CLI to Antigravity CLI transition](https://developers.googleblog.com/an-important-update-transitioning-gemini-cli-to-antigravity-cli/)
- [Antigravity pricing](https://antigravity.google/pricing)
- [OpenCode](https://opencode.ai/)
- [Perplexity Education Pro](https://www.perplexity.ai/help-center/en/articles/12590157-what-is-education-pro)

Happy coding. Use the credits before somebody in finance notices.

## License

This guide is licensed under [Creative Commons Attribution 4.0 International](./LICENSE). Share and adapt it with attribution.
