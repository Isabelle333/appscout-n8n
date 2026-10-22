# Test messages to send to the bot (in Telegram)

| Message | Expected reply | AI requests |
|---|---|---|
| `/help` | The help text | 0 |
| `hello` | "I didn't understand that. Try: …" | 0 |
| `/compare` | "Working on it…", then "Tell me what you need after /compare…" | 1 |
| `/compare accounting software for 5 people` | "Working on it…", then "I can only compare CRM, project management and email marketing…" | 1 |
| `/compare CRM for 10 people under 20 euros per user, needs lead scoring` | "Working on it…", the ranked shortlist, then the .xlsx file; a new row in the Requests tab | 2 |
| `/pending` (admin only) | The rows waiting for a check, flagged rows first | 0 |
| `/verify <tool name>` (admin only) | "Verified: <name> (<category>)" | 0 |
| `/pending` from another account | "I didn't understand that…" (admin commands are hidden) | 0 |

The `.json` files in this folder are mock inputs for the two sub-workflows: open the sub-workflow,
pin the file's content on its trigger (Output panel → Edit → paste → Save), then Execute workflow.
Unpin it afterwards. Never click Execute workflow on appscout_main once it is published.
