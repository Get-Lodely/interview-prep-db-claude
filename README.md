# Interview Prep DB

Real SWE interview questions

Find concrete interview practice questions by company, topic, type or difficulty. Fit them into your available study sessions, practice with hints, or run a mock interview. Claude adapts practice using context you choose to share in the conversation.

## What is included

The software-engineering interview-preparation skill and three read-only MCP
retrieval tools: `get_prep_options`, `search_interview_questions`, and
`get_interview_question`. Questions come from an approved subset sourced from
Lodely; original statements and company associations are returned with links.
Company associations do not predict future interview questions.

Plans, personal experience and completed practice stay in the conversation.
The connector does not save plans, mark completion, change accounts, or return
solutions, paid editorials or hidden tests. No account is needed for retrieval.
Linked Lodely pages offer the statement view; additional app features follow the
app's normal account and access rules.

## Try it

After installing the plugin, start a new conversation and ask:

- Give me interview practice questions for Amazon.
- I have 30 minutes tonight. Help me practice graphs.
- Run a system-design mock interview for Google.

For follow-ups, reuse the same conversation and say what you completed or where
you got stuck. For behavioral coaching, provide your own experience.

## Installation and connection

Load this folder or its ZIP as a custom plugin in Claude. For a local Claude Code
session, run `claude --plugin-dir /path/to/interview-prep-db-claude` from an empty
working folder, then approve the declared MCP connection when prompted.
The anonymous Streamable HTTP endpoint is `https://mcp.lodely.com/claude/mcp`. It must be deployed
and reachable before cloud-hosted Claude clients can connect. A source package
alone does not publish or deploy the server.

## Validation

Run `claude plugin validate . --strict` with Claude Code 2.1.281 or later.
The `evals/` folder carries the five positive and three negative cases from the
approved foundation manifest, adapted to Claude's native evaluation format.
With a working endpoint, run:

```sh
claude plugin eval . --runs 1 --ablation none --mocks off --allow-tools mcp__plugin_interview-prep-db_interview-prep-db__get_prep_options mcp__plugin_interview-prep-db_interview-prep-db__search_interview_questions mcp__plugin_interview-prep-db_interview-prep-db__get_interview_question --no-publish
```

Evaluation uses your Claude subscription/API usage. Results and transcripts must
stay local and are excluded from Git. The routine case also needs a same-chat
follow-up: say the first exercise is complete and request the next one. Verify a
different exercise, including aliases, and the same company/time constraints.
For behavioral coaching, provide a real experience and verify it is not invented.
Local command-line results do not establish web or Cowork compatibility: test
those surfaces before claiming support or submitting the listing.

## Privacy and support

The tools accept bounded practice filters and question IDs, not full conversation
history, resumes or account details. The service records abuse-control state and
aggregate operational usage. Opening a source link can create a browser referral
marker used for attribution. See the [privacy policy](https://www.lodely.com/privacy-policy)
and [terms](https://www.lodely.com/terms-and-conditions).

[Documentation and source](https://github.com/Get-Lodely/interview-prep-db-claude) · [Support](https://www.lodely.com/support) · [Website](https://www.lodely.com/)

## Source and licensing

Package identity, artwork, prompts and coaching guidance are exported from the
approved foundation package. `SOURCE.json` records their hashes for review.
A Claude-only continuity note preserves the user's stated deadline across
completion updates; the original foundation skill is not changed.
Package metadata and documentation are covered by the root LICENSE.
The skill's upstream MIT notice is retained in
`skills/swe-interview-prep/LICENSE`. This repository includes no question dataset;
access to the hosted content is governed by the service terms.
