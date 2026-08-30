# Data model

A trial should be small, explicit, and reproducible.

```json
{
  "id": "trial-...",
  "labId": "time-sense",
  "labVersion": "0.1.0",
  "timestamp": "2026-08-30T00:00:00.000Z",
  "parameters": { "targetMs": 10000 },
  "response": { "estimatedMs": 10422 },
  "metrics": { "absoluteErrorMs": 422 },
  "confidence": 70
}
```

## Research Pack

The export format contains measurements and deterministic summaries, but no name or email by default.

```json
{
  "schemaVersion": "0.1",
  "generatedAt": "...",
  "summary": { "trials": 120 },
  "labs": [],
  "trials": []
}
```
