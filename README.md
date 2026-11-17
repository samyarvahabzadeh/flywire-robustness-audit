# flywire-robustness-audit

**Status: PARKED (fallback project).** Activation condition: if the primary GNN project fails its week-2 feasibility gate, reuse its FlyWire data pipeline here.

## What this is
A systematic robustness audit of headline whole-brain network-statistics claims built on the FlyWire connectome, across these stress dimensions:

1. Synapse-count threshold: {0,1,2,3,5,10,20}
2. Proofreading snapshot: v630 (used by the flagship paper) vs v783 (Codex default)
3. Null models: ER, configuration, spatial, NPC
4. Neurotransmitter-prediction confidence filtering (for NT-dependent claims)

## Why a robustness audit?
- The flagship network-statistics paper (Lin et al., Nature 2024) used threshold=5 and snapshot v630; its authors note some choices (e.g., the rich-club regime cutoff) are somewhat arbitrary, and several results appear in supplements as threshold-sensitivity checks.
- A 2026 compass-circuit study showed reconstruction/proofreading differences can rival genuine inter-individual differences and proposed an explicit quality checklist - no one has generalized that audit to whole-brain claims.

## Assets
- Original analysis notebooks (MIT license): murthylab/flywire-network-analysis (Zenodo archive + GitHub) - the anchor to reproduce first.
- Data: Codex downloads (dataset=fafb), graph-tool for nulls.

## Anchor numbers to reproduce first (Lin et al., Table/abstract)
- 127,978 neurons; 2,613,129 connections at threshold 5 (v630 inputs)
- Giant SCC 93.3%; WCC 98.8%; reciprocity 0.138; clustering 0.0463

## Output
1. Preprint: robustness framework + audited claims (bioRxiv first)
2. Public, reproducible pipeline (this repo)
3. AUDIT_LEDGER.csv as a living public record others can extend

Framing: service, not policing - a 'stability charter' for the field.
