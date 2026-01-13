# PHYSICS CAPABILITIES — Canonical V1

Engine Key: **SPECTRA**  
Authority: Engine Repo (Binding declaration; enforced by CORE Runtime)

## Purpose
Declare supported capability keys and explicit exclusions.

## Required Global Controls
- deterministic_seed: REQUIRED
- fp_mode: strict (no fast-math)
- window_function ∈ {hann, hamming, blackman} (declared)
- sample_rate_hz: REQUIRED
- units tagging required for inputs/outputs where meaningful

## Supported Capabilities
- CAP_SPECTRAL_FFT
- CAP_SPECTRAL_PSD
- CAP_TRANSFER_FUNCTION
- CAP_COHERENCE
- CAP_RESPONSE_ESTIMATION

## Unit Tagging Rules
All outputs MUST be unit-tagged per governance/UNITS_AND_CONVERSIONS.md.

## NOT_SUPPORTED
- CAP_WIND_SPEED
- CAP_RAIN_RATE
- CAP_TSUNAMI_WAVE_DYNAMICS
- CAP_EM_FIELD_COUPLING
- CAP_THERMAL_GRADIENTS
- CAP_STRUCTURAL_FAILURE_SIGNATURES
- CAP_CRYSTAL_RESONANCE
- CAP_LAYERED_MEDIA_RESPONSE (unless explicitly introduced in future V*)
- Any classification / attribution / intent inference

## Notes
- Deterministic transforms only.
- Outputs are numeric descriptors + response curves; no narrative claims.
- Inputs delivered by CORE only.
