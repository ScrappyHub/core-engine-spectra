# SPECTRA REQUIRED ARTIFACTS (Canonical V1)

Engine Key: **SPECTRA**  
Semantics: **DETERMINISTIC_TRANSFORM**  
Authority: Engine Repo (Binding addendum; enforced by CORE Runtime)

This document is an addendum to:
`ScrappyHub/Core-platform/GOVERNANCE/RUN_BUNDLE_SPEC.md`

SPECTRA is a TRUTH_ADJACENT_COMPUTE engine. It performs deterministic spectral measurement only.

---

## Required (in addition to standard RUN_BUNDLE spec)

No additional artifacts are required beyond the standard CORE run bundle.

If SPECTRA emits extra transform artifacts (e.g., FFT bins, PSD tables, coherence matrices, STFT frames), they MUST be:
- listed in `ARTIFACT_INDEX.json`
- hashed in `SHA256SUMS.txt`
- unit-tagged where applicable per `UNITS_AND_CONVERSIONS.md`

---

## Required Output Fields (RUN_OUTPUT.json)

RUN_OUTPUT.json MUST satisfy the engine OUTPUT_SCHEMA and MUST include:
- `semantics = DETERMINISTIC_TRANSFORM`
- `inputs_hash`
- `outputs_hash`

---

## Prohibitions

SPECTRA output MUST NOT include:
- causal/attribution/intent claims
- classifications or conclusions (vertical lens only)
- identity/governance/billing fields
- peer delivery indicators (inputs are delivered by CORE only)
