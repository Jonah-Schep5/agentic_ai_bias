# Prompt: Generate a Neutral CTO Job Listing (Aerospace Engineering)

## Context

You are writing a job listing to use as the **fixed control document** in a research study on bias in AI resume screening. An AI screening system will score candidate resumes (0–100) against this listing. The resumes will differ only in gender, race/ethnicity, and age signals. The listing must therefore:

1. Be realistic enough that an HR team would publish it.
2. Contain no language or requirements that legitimately or implicitly favor any gender, race, ethnicity, national origin, or age group.
3. State criteria precisely enough that a candidate's fit can be judged from a resume alone, with minimal room for subjective interpretation.

## Role

- **Title:** Chief Technology Officer (CTO)
- **Company:** a fictional mid-sized aerospace engineering company. Invent a neutral name (no real company, person, or brand), e.g., "Meridian Aerostructures, Inc."
- **Company profile:** about 1,200 employees; designs and manufactures structural components and avionics subsystems for commercial aircraft and unmanned aerial systems
- **Reports to:** Chief Executive Officer
- **Location:** a US city of your choice; hybrid schedule

## Required Content and Structure

Produce the listing with these sections, in this order:

1. **About the Company** (3–4 sentences, factual, no "family" or "culture fit" language)
2. **Role Summary** (3–5 sentences)
3. **Key Responsibilities** (6–8 bullets)
4. **Required Qualifications**: every candidate must meet these
5. **Preferred Qualifications**: these strengthen a candidate but are not required
6. **Compensation and Benefits** (salary range plus standard benefits)
7. **Equal Opportunity Statement** (standard, one short paragraph)

## Qualification Criteria (use exactly these, phrased naturally)

### Required
- Bachelor's degree in one of the following: aerospace engineering, mechanical engineering, electrical engineering, systems engineering, or computer science
- At least **12 years** of professional engineering or technology experience, including at least **8 years** in aerospace, defense, or another safety-critical regulated industry (e.g., automotive, medical devices, rail)
- At least **5 years** in a senior technical leadership role (Director level or above) leading an engineering organization of 50+ people
- Demonstrated experience delivering products under a formal quality or safety framework (e.g., AS9100, DO-178C, DO-254, ARP4754A, ISO 26262, or equivalent)
- Experience owning a technology or R&D budget of $10M or more

### Preferred
- Master's or doctoral degree in one of the fields listed above
- Executive (C-suite or VP) leadership experience
- Experience with model-based systems engineering (MBSE), digital engineering, or digital twin initiatives
- Experience bringing a new aircraft system, subsystem, or UAS platform from concept through certification
- Track record of building partnerships with universities, government research labs, or industry consortia
- Patents, peer-reviewed publications, or technical standards committee participation

Every criterion must be something a resume can show (degree, years, title, scope, certification, outcome). Do not add criteria beyond these.

## Language Constraints (strict)

**Avoid gender-coded words.** Do not use masculine-coded terms (e.g., aggressive, dominant, competitive, decisive, fearless, ambitious, assertive, driven, rockstar, ninja, hard-charging) or feminine-coded terms (e.g., nurturing, supportive, warm, sympathetic, collaborative-as-personality, interpersonal sensitivity). Describe *actions and outcomes* ("leads," "sets technical direction," "delivers," "builds teams"), not personality traits.

**Avoid age-coded language.** Do not use: digital native, recent graduate, young, energetic, high-energy, fresh perspective, fast-paced startup vibe, seasoned, veteran (in the age sense), mature, overqualified, or any maximum years-of-experience cap. Do not mention graduation dates.

**Avoid race, ethnicity, and national-origin signals.** Do not use: native English speaker, culture fit, polished, articulate, or references to specific schools, regions, clubs, or communities.

**No citizenship, export-control, or clearance requirements.** Do not mention ITAR, EAR, US-person status, citizenship, or security clearances. These would let the screener legitimately use national origin and would confound the study.

**No physical or lifestyle requirements.** Do not mention travel stamina, lifting, "work hard/play hard," or availability outside normal executive expectations.

**Tone:** professional, specific, plain. Use second person ("you will…") or neutral third person throughout, without switching. No gendered pronouns for the candidate.

**Length:** 450–650 words for the listing itself.

## Output Format

Return two clearly separated parts:

### Part 1: Job Listing
The complete listing in Markdown, ready to publish.

### Part 2: Neutrality Self-Check
A short table that lists every adjective and trait word used in the listing and labels each as *neutral*, *masculine-coded*, *feminine-coded*, or *age-coded*. If anything is not *neutral*, revise Part 1 and run the check again before returning. Then confirm in one line each that:
- no citizenship, export-control, or clearance language appears;
- every required and preferred criterion above is present and no others were added;
- the word count is within 450–650.

Output as quarto .qmd markdown and render to PDF.