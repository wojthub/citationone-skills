# CitationOne skills

[![skills.sh](https://skills.sh/b/wojthub/citationone-skills)](https://skills.sh/wojthub/citationone-skills/citationone)

Agent skills for [CitationOne](https://citationone.com) - audits of how likely AI search engines (Google AI Overviews, ChatGPT, Perplexity) are to cite a web page.

## Skills

| Skill | What it does |
| --- | --- |
| [`citationone`](skills/citationone/SKILL.md) | Runs CitationOne audits through the CitationOne MCP server and turns the results into client-ready SEO priorities: confirms the credit cost before an audit, reads the CQS score against the top 10 Google results, merges several pages of one client into one priority list, compares audits before and after changes, and writes a client summary. |

## Install

```bash
npx skills add wojthub/citationone-skills
```

Install globally for Claude Code only:

```bash
npx skills add wojthub/citationone-skills --skill citationone -a claude-code -g
```

Manual install (Claude Code / Claude Desktop):

```bash
mkdir -p ~/.claude/skills/citationone
curl -o ~/.claude/skills/citationone/SKILL.md https://app.citationone.com/skills/citationone/SKILL.md
```

In claude.ai, zip the `citationone` folder and upload it in the skills settings.

## Requirements

The skill uses the CitationOne MCP server (tools `start_audit`, `get_audit`, `list_audits`, `get_credits`). Connect it with an API key from [app.citationone.com](https://app.citationone.com) - setup guide: https://app.citationone.com/api-docs#mcp.

Each audit costs 1 credit. Reading results is free.

## Support

Report problems in [Issues](https://github.com/wojthub/citationone-skills/issues).

## License

MIT
