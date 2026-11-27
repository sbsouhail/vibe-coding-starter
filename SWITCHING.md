# Moving a project between tools

GitHub is the hub: every tool reads from your team repo or writes to it, so no work is lost when credits run out.

| Tool | Connection to GitHub | Can it pick up a project from elsewhere? |
| --- | --- | --- |
| Google AI Studio | Two-way sync (Settings › GitHub), or ZIP download | Yes, + menu › Import from GitHub |
| Bolt | Two-way sync | Yes, imports any repo you can push to |
| Lovable | Two-way sync | No, it can't import an existing repo: start there |
| Cursor | Clone, edit, push | Yes, any repo |

**Rule of thumb:** AI Studio, Bolt and Cursor can pick up a project from anywhere. Lovable can only hand one off.

## To switch tools

1. Push the last working version to GitHub.
2. Import the repo in the next tool (for example Bolt › GitHub › Import).
3. Re-add your secrets: API keys don't travel with the code. An app exported from AI Studio needs `GEMINI_API_KEY` set again (see [KEYS.md](KEYS.md)).
4. Give the new AI context with a [HANDOVER.md](HANDOVER.md) note kept in your repo. Start your first prompt with: "Read HANDOVER.md first."

Sources: [Google AI Studio docs](https://ai.google.dev/gemini-api/docs/aistudio-build-mode) · [Bolt GitHub docs](https://support.bolt.new/integrations/git) · [Lovable Git sync docs](https://docs.lovable.dev/integrations/git-sync-overview)
