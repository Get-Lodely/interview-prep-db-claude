---
{"name": "unavailable-company-coverage", "description": "Unavailable company coverage", "runs": 1, "max_turns": 24, "timeout_seconds": 240, "allowed_tools": ["Read", "Skill", "mcp__plugin_interview-prep-db_interview-prep-db__get_prep_options", "mcp__plugin_interview-prep-db_interview-prep-db__search_interview_questions", "mcp__plugin_interview-prep-db_interview-prep-db__get_interview_question"], "expected_outcome": "Use get_prep_options to check the exact requested company. If no company matches, explain that the question subset has no matching company coverage; do not claim that the company itself does not exist. Do not invent a company ID, label another company's questions as matches, or retrieve substitute questions without the user's agreement. Offering to broaden the scope is optional; actually broadening it requires the user's agreement."}
---

Give me interview questions tagged with ZzNoSuchCompany4817. Do not substitute another company.
