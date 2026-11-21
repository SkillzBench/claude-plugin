# SkillzBench for Claude Code

Benchmarked, security-scanned agent skills for Claude Code, served through one MCP connector.

```text
/plugin marketplace add SkillzBench/claude-plugin
/plugin install skillzbench@skillzbench
```

Then run `/mcp`, pick **skillzbench**, choose **Authenticate**, and sign in (free). Pick skills or a starter pack at
[skillzbench.com](https://skillzbench.com/skills). Claude sees a short list of what you switched on and loads a skill
only when a task calls for it.

**No account yet?** Try the read-only starter set first:

```bash
claude mcp add --transport http skillzbench-trial https://mcp.skillzbench.com/try
```

- Every skill is security-scanned and pinned to the scanned version.
- 236 skills are benchmarked head-to-head, with vs. without the skill; wins and losses are both published.
- Skills that bundle scripts are served only when the license is permissive and the scan is clean. Claude shows you a
  script before running it.

[How we measure](https://skillzbench.com/methodology) · [All skills](https://skillzbench.com/skills) · team@skillzbench.com
