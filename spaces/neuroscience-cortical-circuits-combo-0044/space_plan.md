# Space Plan - neuroscience-cortical-circuits-combo-0044

## Scientific Scope
- Domain: neuroscience
- Theme: cortical_circuits
- Base models: neuroscience-neuroml-layer-2-3-continuous-accommodating-neurogliaform-nmlcl000497-model, neuroscience-neuroml-layer-2-3-continuous-accommodating-neurogliaform-nmlcl000498-model, neuroscience-neuroml-layer-2-3-continuous-accommodating-neurogliaform-nmlcl000499-model

## Wiring Plan
- Comparative mode with monitor-only routing.
- Each base model state-like output connects to monitor ports `state_a..state_d`.
- No direct causal links among base models unless explicitly upgraded later.

## Visualization Plan
- Include `StateComparisonMonitor` and `StateMetricsMonitor`.
- Require at least:
  - one timeseries visual,
  - one summary table visual.

## Validation Gates
- space schema validity
- wiring endpoint validity
- smoke run success
- repo manifest/entrypoint validators pass
