# clauderesearch.ai

Public website for [`claude_researcher`](https://github.com/danparshall/claude_researcher) — the friendly, non-developer entry point ([claude_researcher#11](https://github.com/danparshall/claude_researcher/issues/11)).

Static HTML/CSS with one tiny inline script (copy-to-clipboard). No build tools. Hosted on GitHub Pages at `clauderesearch.ai`.

## Design notes

- **The human pastes once; the agent hops.** The two paste blocks on the page are self-contained prompts. The setup block tells the agent to fetch the `claude_researcher` README on `main` and follow its Quick-start prompt (which pins a specific commit SHA). This keeps the site drift-free: re-pinning the bootstrap SHA (`tools/repin.py` upstream) never requires touching this repo.
- **Screenshots** are copies of `claude_researcher/template/reference/screenshots/` (see its `CAPTURED.md` for capture provenance). Re-copy when upstream re-captures.

## Local preview

```
python3 -m http.server 8000
```
