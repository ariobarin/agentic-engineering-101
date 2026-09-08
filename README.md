# Agentic Engineering 101: AI Coding Tools for Students

University students get a lot of free credits and discounted access to coding agents. Seriously, take advantage of it while you can. This is a guide to choosing a tool, understanding what you're paying for, and getting useful work out of it.

> Reviewed September 8, 2026. Prices are USD before tax. Check the linked offer before paying; eligibility, models, and limits change.

## Where I'd start

My setup is built around **Codex**. I want to give it a repository and a problem, talk through the approach, and get back a change I can review. The interface matters too, especially when I'm talking through ideas or working on several tasks at once.

Start with the access you already have. Pick a small project you actually want to build and use it enough to find out where you get stuck. You don't need three subscriptions before you've made anything.

| Tool | Access worth knowing about | What to check |
| --- | --- | --- |
| [Codex](https://learn.chatgpt.com/docs/pricing) | Plus is $20/month; Pro 5x is $100 and Pro 20x is $200. | [Eligible university students in the US and Canada can claim $100 in ChatGPT credits for Codex](https://developers.openai.com/community/students). These are not API credits. One grant per student; expires after 12 months. |
| [Claude Code](https://claude.com/pricing) | Included in Pro, $20 billed monthly; Max starts at $100. | [Claude and Claude Code share plan limits](https://support.claude.com/en/articles/11145838-use-claude-code-with-your-pro-or-max-plan). Check whether your university provides [Claude for Education](https://claude.com/solutions/education). |
| [GitHub Copilot Student](https://docs.github.com/en/copilot/how-tos/copilot-on-github/set-up-copilot/enable-copilot/set-up-for-students) | Free for verified students, with unlimited code completions and an AI-credit allowance. | The [Student plan uses automatic model selection and excludes third-party agents](https://docs.github.com/en/copilot/get-started/plans). It does not give you everything in paid Pro. |
| [Cursor](https://cursor.com/pricing) | Free tier; Pro starts at $20/month. | The [student page](https://cursor.com/students) currently points to campus and online event promotions. It no longer promises everyone a free year. |
| [Gemini CLI](https://geminicli.com/docs/resources/quota-and-pricing/) | Up to 1,000 model requests/day through a personal Google account with Code Assist for individuals. | The unpaid API-key route has a different allowance: 250 requests/day to Flash. One agent task can take multiple model requests. |
| [OpenCode](https://opencode.ai/docs/) | Open-source agent with a terminal interface and support for different model providers. | Installing the agent is free. Model usage depends on the provider you connect. |

[Antigravity](https://antigravity.google/pricing) also has a free individual tier with weekly limits. [AI Studio](https://ai.google.dev/gemini-api/docs/pricing) is useful for model and API experiments; free access and data-use terms depend on the model and tier. For research, [Perplexity Education Pro](https://www.perplexity.ai/help-center/en/articles/12590157-what-is-education-pro) is a discounted plan for verified students and educators. Follow its citations through to the original work.

Model choice changes faster than this guide. For a shortlist, look at [Artificial Analysis](https://artificialanalysis.ai/) or my [Which LLM](https://github.com/ariobarin/which-llm), then try the candidates on your own task. Compare the finished result, time spent correcting it, and cost. A model score and a coding-agent score measure different things, and cheap tokens can still produce an expensive task.

## How much usage do you actually get?

“5x usage” tells you very little about whether you can work all afternoon. A subscription can give a heavy user far more usage than buying the same tokens through an API, but the workload matters.

**API-equivalent cost** means pricing the tokens you used at public API rates. It compares usage with a hypothetical API bill. It is not your subscription bill or a balance you can spend, and it does not tell you what the provider spent serving you.

### What people have measured

In its **June 10, 2026** [subscription experiment](https://x.com/SemiAnalysis_/status/2064815044085318040), SemiAnalysis reported approximate monthly API-equivalent maxima of **$14,000 for the $200 ChatGPT Pro plan** and **$8,000 for the $200 Claude Max plan**. It bought one subscription per tier and ran long coding tasks until the weekly limits were exhausted. The [readable thread](https://threadreaderapp.com/thread/2064815044085318040.html) describes the method; [Tom's Guide reproduces the chart](https://www.tomsguide.com/ai/the-math-doesnt-work-why-your-usd200-ai-subscription-is-secretly-worth-thousands), rather than repeating the experiment.

Those are historical estimates, not September quotas. The public thread does not provide raw usage logs or the exact monthly extrapolation. Dividing the figures by 20 does not establish what today's entry-level plans provide.

[u/xzlllwyyy's Codex log audit](https://www.reddit.com/r/codex/comments/1w1ne3f/my_first_week_after_switching_from_claude_code_to/), retrieved September 8, 2026, estimates **about $102 of API-priced usage across 16 GPT-5.6 Sol sessions**. Most of that estimate comes from cached input, context the model rereads at a discounted rate. The author describes the counting method but does not publish raw logs. This is a reported workload, not a plan ceiling.

### Measure your own week

Use the provider's usage page to see limits and reset times. [ccusage](https://ccusage.com/guide/) can estimate API cost from local logs; check its [model-pricing and fallback rules](https://ccusage.com/guide/codex/) before trusting a total. Even usage counters can [count the same event twice](https://github.com/ccusage/ccusage/pull/1687).

Record the work you finished and when limits interrupted it. Compare that with the subscription fee or API bill before upgrading. Exhausting a plan with repeated failed attempts is not the same as getting value from it.

## How I work with agents

### Get the understanding right

For an unfamiliar project or a broad change, I want the agent to inspect what exists and explain what it thinks I'm asking for before it starts changing things. Give it the actual problem, the relevant files, examples, and constraints. If the explanation is wrong, fix that first.

I dictate a lot. It lets me talk through the reasoning, including the parts I'm unsure about. When delegating, pass along the relevant original explanation too. An agent's summary can preserve the facts and lose the reason I cared about them. This matters especially for writing and design.

[Wispr Flow](https://wisprflow.ai) is one option for dictation. If you want to use my referral links, here are [Flow](https://wisprflow.ai/r?ARIO16) and [Perplexity](https://plex.it/referrals/8N3ELADE).

### Make the project easy to operate

Put the setup and verification commands in the repository's [AGENTS.md](https://learn.chatgpt.com/docs/agent-configuration/agents-md), or the tool's equivalent. Include the constraints the agent cannot infer from the code. Keep it short enough to read as a whole.

Fix missing dependencies, expired sessions, or broken test commands before treating a failed run as evidence that the model cannot do the task. Give it access to useful diagnostics, including language-server tools where supported. Then check the actual changed behavior.

### Delegate work that can be done independently

A subagent can investigate a separate question while the main agent keeps working. Give it enough context, a clear responsibility, and a result to bring back. Review what comes back; the first answer is not automatically good enough.

For independent changes, use [separate worktrees](https://learn.chatgpt.com/docs/environments/git-worktrees) so each task has its own checkout and branch. If agents share a checkout, give them distinct file ownership. A branch name alone does not isolate files. Keep each pull request focused enough to review.

### Verify what you wanted

For a bug, get a reproduction that fails before the fix and succeeds afterward. For a UI change, use the interface and check the interaction you asked for. A passing build cannot tell you whether the page makes sense.

Use the checks that could expose a real failure in the change. Read the diff, look at the evidence, and stop adding checks once the remaining uncertainty is resolved. Simon Willison's [August 22 note on verification](https://simonwillison.net/2026/Aug/22/more-than-just-code-review/) makes a useful point: reviewing every line is only one way to establish that a change is correct.

### Add skills when they fix something

The agent already knows a lot. What I want from a skill is better judgment where its default behavior keeps going wrong: diagnosing before guessing, checking sources, or pruning a draft instead of accepting the first thing it wrote.

I maintain [Compass](https://github.com/ariobarin/compass) for my Codex instructions, skills, and agents. I took inspiration from [Lauren Tan's pstack](https://github.com/cursor/plugins/tree/main/pstack/skills) and [Matt Pocock's skills](https://github.com/mattpocock/skills), then adapted the parts that fit how I work. Things have to earn their place. Read the skill, understand the behavior it is meant to change, and see whether it helps before adding another one.

Useful examples are Compass's [diagnosing-bugs](https://github.com/ariobarin/compass/blob/main/codex/skills/diagnosing-bugs/SKILL.md), [ground-in-sources](https://github.com/ariobarin/compass/blob/main/codex/skills/ground-in-sources/SKILL.md), and [test-for-risk](https://github.com/ariobarin/compass/blob/main/codex/skills/test-for-risk/SKILL.md). The [Agent Skills specification](https://agentskills.io/specification) explains the file format.

Before connecting private coursework, research, or company code, check the tool's data-use settings and the rules governing that material. Keep credentials out of prompts. A free plan is not permission to upload somebody else's work.

## License

This guide is licensed under [Creative Commons Attribution 4.0 International](./LICENSE). Share and adapt it with attribution.
