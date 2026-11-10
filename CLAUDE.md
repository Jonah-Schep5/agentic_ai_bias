# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this repo is

A research project (ADS 5984) auditing bias in LLM-based resume screening. LLMs (VT ARC hosted models, and possibly Anthropic and Grok models) score candidate resumes 0–100 against one fixed job posting. Resumes differ only in demographic signals: race/ethnicity, gender, and age.

The repo is at an early stage. So far it contains only prompts and the job posting. There is no code, test suite, or build system yet.

## Files

- `prompt.md`: the original study prompt.
- `improved_prompt.md`: the current study design and the source of truth for methodology. It covers four fit tiers (high, borderline, mid, low), a name-free baseline and manipulation check, demographic variants, the controls held constant across variants, the scoring protocol, and the pre-registered analysis plan. Read it before generating resumes, scoring code, or analysis.
- `cto_job_listing.qmd`: the fixed job posting produced from `improved_prompt.md`. It is the **control document for the whole study**. Do not change its wording unless asked, because any change invalidates comparisons across runs.
- `cto_job_listing.html` / `.pdf` / `cto_job_listing_files/`: rendered output, committed to the repo.
- `backup/`: earlier prompt and listing drafts (e.g., `job_listing_prompt.md`, which used a different 12-year/8-year requirement set). These are superseded and kept only for reference.

## Commands

Render the job posting (Quarto is at `/opt/quarto/bin/quarto`):

```bash
quarto render cto_job_listing.qmd            # html + pdf
quarto render cto_job_listing.qmd --to pdf   # single format
```

## Study constraints to preserve when adding resumes or scoring code

These come from `improved_prompt.md`:

- Base resumes are generated name-free. Demographic variants of one base resume must keep identical content, line count, accomplishments, work authorization ("U.S. Citizen"), clearance status, and visible experience window (the most recent 15–20 years). Age is signaled only through graduation year or an "earlier career" line. Any identity-linked affiliation must be balanced by a neutral affiliation of the same length in the control version.
- Scoring uses one resume per call in a fresh context, a fixed system prompt, the posting verbatim, and a fixed reported temperature, with 3–5 samples per resume. Output is JSON `{"score": <0-100>, "rationale": "..."}`. Log the model ID and version, timestamp, refusals, and malformed outputs.
- Names for race/gender signals come from validated lists (Gaddis 2017; Elder & Hayes 2023), with several names per cell.

## Notes

- `.env` is gitignored and expected to hold API credentials for model endpoints.
