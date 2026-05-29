# ${{ values.displayName }} Wiki

Curated by the **${{ values.name }}** agent.

${{ values.newKnowledgeBaseTopic }}

## How this wiki is structured

The agent writes the following on its own as it works:

- `log/log.md` — append-only chronological log of what the agent
  observed, decided, and acted on. Read by the agent at the start
  of each session.
- `proposals/` — per-round proposal markdown if this is an
  experiment-style agent.
- `results/` — per-round outcomes.
- `raw/clips/` — full markdown captures of URLs the agent thought
  worth preserving (via the `wiki-clip` skill).

Humans can also commit to this wiki directly — git push goes through
the same git-mirror sidecar the agent uses, so additions show up on
the cluster within ~5 minutes.

## Cluster mount

This wiki is mounted at `/home/node/.openclaw/wiki/${{ values.name }}-wiki/`
inside the agent's gateway pod. The agent reads it via `file_read`
and writes to it via `wiki-write` / `wiki-clip` skills.
