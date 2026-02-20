# COMBO_0074 - Neuroscience Cortical Circuits

## Scientific Question
How do cortical circuit motifs transform and propagate activity?

## Biological Context
Neuronal dynamics, network signaling, and emergent circuit behavior.

## Mechanistic Assumptions
- Model implementations are used as published in their curated manifests without biological reinterpretation.
- Time integration uses a shared global tick compatible with model min_dt constraints.
- Comparative (non-causal) mode is used because full deterministic IO coverage for causal coupling was not satisfied.

## Why These Models Belong Together
The combination was selected from a shared domain/theme bucket with deterministic compatibility checks.
- `neuroscience-neuroml-layer-2-3-burst-irregular-bitufted-cell-5-nmlcl000206-model`: Neuroscience: Layer23BurstIrregularBituftedCell5Nmlcl000206Model
- `neuroscience-neuroml-layer-2-3-burst-irregular-double-bouquet-cell-1-nmlcl000207-model`: Neuroscience: Layer23BurstIrregularDoubleBouquetCell1Nmlcl000207Model
- `neuroscience-neuroml-layer-2-3-burst-irregular-double-bouquet-cell-2-nmlcl000208-model`: Neuroscience: Layer23BurstIrregularDoubleBouquetCell2Nmlcl000208Model
- `neuroscience-neuroml-layer-2-3-burst-irregular-double-bouquet-cell-3-nmlcl000209-model`: Neuroscience: Layer23BurstIrregularDoubleBouquetCell3Nmlcl000209Model

## Wiring Rationale
- Comparative (non-causal) mode: no direct causal links were created.

## Visualization Strategy
- Monitor-driven visualization is required for this space.
- State streams are routed into explicit monitor ports (`state_a..state_d`) to avoid signal overwrite.
- At minimum, monitor visuals include one timeseries panel and one summary table.
- Rationale: A dedicated monitor model receives all participating model state streams (`state_a..state_d`) so trajectories can be compared in one place without claiming causal coupling when IO semantics are incomplete.

## Expected Behaviors
- Model output trajectories under shared runtime settings.
- Cross-model agreement/divergence in key state or metric signals.
- Relative behavior comparison without causal linkage claims.

## Known Limitations
- No new biology is introduced beyond what upstream models encode.
- Cross-model semantic matching is rule-based and may under-connect uncertain routes.

## Source Provenance
- neuroscience-neuroml-layer-2-3-burst-irregular-bitufted-cell-5-nmlcl000206-model :: neuroml_db:NMLCL000206 :: https://neuroml-db.org/model_info?model_id=NMLCL000206
- neuroscience-neuroml-layer-2-3-burst-irregular-double-bouquet-cell-1-nmlcl000207-model :: neuroml_db:NMLCL000207 :: https://neuroml-db.org/model_info?model_id=NMLCL000207
- neuroscience-neuroml-layer-2-3-burst-irregular-double-bouquet-cell-2-nmlcl000208-model :: neuroml_db:NMLCL000208 :: https://neuroml-db.org/model_info?model_id=NMLCL000208
- neuroscience-neuroml-layer-2-3-burst-irregular-double-bouquet-cell-3-nmlcl000209-model :: neuroml_db:NMLCL000209 :: https://neuroml-db.org/model_info?model_id=NMLCL000209

## How to Run
```bash
python run_local.py --duration auto --tick-dt auto
```

## How to Interpret Outputs
Use output trajectories and summary metrics to compare mechanistic consistency across constituent models.
Interpret comparative spaces as non-causal side-by-side simulation views.
