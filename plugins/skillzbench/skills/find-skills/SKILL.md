---
name: find-skills
description: Find a benchmarked, security-scanned skill for the current task on SkillzBench. Use when the user asks "is there a skill for X", wants to make Claude better at a kind of task, or asks what SkillzBench skills they have.
---

# Find skills on SkillzBench

The `skillzbench` MCP server is connected through this plugin. On first use, run `/mcp`, pick **skillzbench** and choose **Authenticate** to sign in (a free account is created in the browser if needed).

1. **What's switched on:** if the user's enabled skills are already listed as skills from this server (named `skillzbench:<slug>`), load the one that fits the task that way. Otherwise call `list_enabled`, and if one fits, call `get_skill` with its slug and follow it.
2. **Find new ones:** call `search_skills` with a short description of the task. Prefer results whose `benchmark.status` is `published` with a positive value, then higher `trust_score`. Only `servable: true` skills can be loaded.
3. **Add one:** call `request_enable` with the slug. If the response has an `approval_url`, give it to the user. They approve in one click.
4. **Tell the user** which skill you used, and link its page: `https://skillzbench.com/skills/<slug>`.

Just want to try it without an account? The no-login trial connector is `https://mcp.skillzbench.com/try` (a fixed set of 30 top skills).
