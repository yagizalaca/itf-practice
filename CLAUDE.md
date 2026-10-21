# Project context for Claude Code

## What this repo is
A small practice project: estimating **individual theta frequency (iTF)** from EEG power spectra using **specparam (FOOOF)**. It is a warm-up for a university Practical Project on theta-tACS in older adults with Subjective Cognitive Decline (SCD), where stimulation frequency will be tuned to each participant's iTF.

## The person you are working with
- MSc student in Neurocognitive Psychology. Strong in MATLAB and EEGLAB; Python is decent but less practiced.
- Is using this repo to **learn** Python, Git and GitHub. Learning matters more than speed.
- Explain in **Turkish** by default. Keep technical terms in English (e.g. "power spectrum", "commit").
- When relevant, show the MATLAB equivalent of Python code.

## How to respond
- Start with the next concrete action, not background.
- Use short numbered steps; one bounded action per step.
- Explain each code change in plain words before or after making it.
- Prefer small changes the user can run and check, over large rewrites.
- End with one small next step.

## Environment
- macOS (Apple Silicon), VS Code.
- Conda environment: `itf` (Python 3.11). Activate with `conda activate itf`.
- Installed: mne 1.13, specparam 2.0.0rc7 (API: `from specparam import SpectralModel`; `model.get_params("periodic")`, `model.get_params("aperiodic")`, `model.get_metrics("gof")`), numpy, scipy, matplotlib, ipykernel.

## Files
- `itf_practice.ipynb`: simulated EEG (1/f background + 6 Hz theta + 10 Hz alpha), raw spectrum vs FOOOF-corrected spectrum, iTF and IAF-derived fallbacks (IAF/2 harmonic, IAF/1.618 golden mean).

## Key concepts already understood
- Raw spectral maximum is biased by the 1/f slope, so raw max ≠ iTF; remove the aperiodic component first.
- If no theta peak is found, iTF can be derived from IAF (÷2 or ÷1.618).

## Planned next steps
1. Run the notebook and check results.
2. Commit and push to GitHub (learn add / commit / push).
3. Later: try the same pipeline on real EEG (e.g. MNE sample data).
