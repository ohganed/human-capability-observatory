# Human Capability Observatory

**自分という人間を観測する研究所。**

Human Capability Observatory (HCO) is a local-first, AI-optional experimental app for exploring perception, timing, pattern recognition, intuition, metacognition, and other human capabilities.

## Core principle

The core app does **not require AI**.

1. Present a controlled stimulus.
2. Record the human response.
3. Measure timing / accuracy / confidence.
4. Analyze deterministically.
5. Store locally.
6. Export only the data the user chooses.
7. If desired, manually give that export to an AI for secondary interpretation.

AI never sits between the raw measurement and the primary result.

## Scientific stance

HCO neither assumes nor denies unknown human capabilities. It measures first.

- Do not label a result as a “sixth sense.”
- Separate observation from interpretation.
- Compare against chance where applicable.
- Prefer repeated sessions and replication.
- Treat AI output as hypotheses, never as measured facts.

## Included prototype labs

- **Time Sense Lab** — estimate 10 seconds without a clock.
- **Quantity Sense Lab** — estimate the number of briefly displayed dots.
- **Pattern Sense Lab** — predict the next item in a deterministic hidden pattern.

The architecture is designed to grow to 100+ labs.

## Run locally

No build step is required.

```bash
python3 -m http.server 8000
```

Then open `http://localhost:8000`.

## Data policy

- Local-only by default (`localStorage` in this prototype).
- No account.
- No API key.
- No automatic upload.
- Export is manual.
- AI analysis is optional and manual.

See [ARCHITECTURE.md](ARCHITECTURE.md), [docs/LAB_CATALOG.md](docs/LAB_CATALOG.md), and [docs/DATA_MODEL.md](docs/DATA_MODEL.md).
