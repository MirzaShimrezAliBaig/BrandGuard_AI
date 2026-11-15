# Technical notes

## Review sequence

`Content input -> Local policy checks -> Finding aggregation -> Risk score -> Suggested correction -> Re-review -> Human decision`

## Rule groups in this prototype

- `CLM-04`: numerical, guaranteed, superlative or otherwise unsupported claims.
- `TRM-008`: preferred audience wording and AI-powered terminology.
- `BRD-02`: hype language and exaggerated promotional tone.
- `ACC-03`: very long sentences/readability.
- `FACT-02`: broad universal statements without approved scope.
- `VIS-01`: registered asset filename and sample colour heuristic.

## Data model (browser local state)

- `knowledge[]`: category, approved text, source and ID.
- `history[]`: reviewed content, findings, score and status.
- `approvals[]`: content snapshot, risk, findings and reviewer decision/comment.
- `activity[]`: timestamped events.
- `settings`: switches for optional checks and governance preferences.

## Important limitations

- Local storage is not a secure multi-user data store.
- Sample knowledge is illustrative and must be replaced with the organisation's verified guidelines and facts.
- Rule-based checks are intentionally limited and can produce false positives/negatives.
- Image colour/filename checks are only heuristics; no image understanding model is connected.
- Production deployment needs security controls, tests, monitoring, backups, a real API/backend and a proper RAG evaluation process.
