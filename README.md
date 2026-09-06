# Echo-HF — 5-year heart-failure risk calculator

Individualized 5-year risk of progression to symptomatic heart failure (HF) in adults
without current symptomatic HF, from five variables present in a routine
echocardiographic report: age, LA diameter, LV mass index, LVEF, and global
longitudinal strain (average).

**Use it:** open the published page, or download `index.html` and open it in any
browser — the page is fully self-contained (no server, no external libraries, no
data leaves the browser).

**What it implements:** the trained Echo-HF XGBoost model (100 depth-1 trees),
embedded exactly, with a Cox recalibration mapping the score to absolute 5-year risk
(fitted on the KNUH training subset). The complete model specification is readable in
this file's source.

**Provenance:** developed in 43,093 adults undergoing echocardiography (Kyungpook
National University Hospital, Korea) and externally validated in 4,448
community-dwelling adults (ARIC, US): held-out test AUC 0.82, external AUC 0.77,
external calibration O/E 0.96 (slope 0.95).

**Intended use & limitations:** a research tool for risk stratification — not a
diagnostic device. It does not establish that acting on the estimate improves
outcomes. Estimates are least reliable at the extremes of the score and in
populations differing substantially from the development and validation cohorts.
Clinical decisions remain the responsibility of the treating clinician.

**Citation:** manuscript under review (*JACC: Heart Failure*); citation will be
added upon publication.

Analysis code is available from the corresponding author on reasonable request.
Patient-level data are not part of this repository and cannot be shared here.
