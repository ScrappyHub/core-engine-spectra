# SPECTRA — Spectral Analysis & Deterministic Frequency Instruments

Engine Key: **SPECTRA**  
Engine Role: **TRUTH_ADJACENT_COMPUTE**  
Domain: **Spectral measurement (frequency/time-frequency)**

SPECTRA performs deterministic spectral measurement on sealed numeric signals and fields. It produces reproducible frequency-domain outputs (FFT/PSD/band energy/coherence) with strict numeric controls.

## What SPECTRA Computes (Deterministic, V1)
- FFT (real/complex), rFFT
- Power Spectral Density (PSD): Welch / periodogram (deterministic windowing)
- Band energy and spectral centroids
- Cross-spectrum and coherence (deterministic)
- Transfer functions (two-channel inputs)
- Time-frequency: STFT (deterministic hop + window)

## Determinism Contract (V1)
SPECTRA must be bit-stable under:
- fixed sample order
- fixed window function
- fixed normalization rules
- fixed floating-point mode (**float64 only**)
- fixed zero-padding policy

No nondeterministic sources (no RNG; no wall-clock behavior).

## Prohibitions
SPECTRA does NOT:
- invent data
- infer identity, intent, or attribution
- classify people or sources
- publish independently

## Governance
SPECTRA is governed by CORE law. All outputs MUST be sealed and manifest-bound at run finalize.

## Repository Layout
- `MANIFEST/` — manifest + input/output schema + coupling rules
- `SEALING/` — sealing spec
- `GOVERNANCE/` — engine governance (engine-specific rules only)
- `CAPABILITIES/` — capability declaration (binding)
- `RUN_BUNDLE/` — run bundle expectations (spec only)
