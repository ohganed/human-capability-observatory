# Architecture

## System boundary

```text
Human
  ↓
Stimulus Engine
  ↓
Response Capture
  ↓
Measurement Layer
  ↓
Deterministic Analysis
  ↓
Local Data Store
  ↓
Research Pack Export
  ↓ (manual only)
Optional external AI analysis
```

## Invariants

1. **AI-independent core** — all experiments and primary statistics work without AI.
2. **Observation / interpretation separation** — measured facts and hypotheses are stored separately.
3. **Local-first** — experiment data remains on the device unless the user exports it.
4. **Manual AI boundary** — the app does not call AI APIs in v1.
5. **Reproducibility** — each trial records lab version and relevant parameters.
6. **No extraordinary-claim shortcut** — unusual results trigger replication, not conclusions.

## Planned modules

- `LabRegistry` — lab metadata and versions.
- `StimulusEngine` — controlled visual/audio/timing stimuli.
- `TrialRecorder` — responses, timestamps, confidence, parameters.
- `AnalysisEngine` — deterministic summaries and chance comparisons.
- `LocalStore` — local persistence.
- `ResearchPackExporter` — privacy-minimized JSON export.
- `StateProtocol` — optional pre/post condition comparisons.

## Safety boundary

The app should not diagnose neurological, psychiatric, medical, or paranormal conditions. It is an exploratory measurement tool.
