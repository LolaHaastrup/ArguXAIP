# ArguXAIP — Bus–Train Collaborative Journey

An Argumentation-Based Framework for Explaining Scheduled Temporal Plans, demonstrated
on a bus–train collaborative journey scenario.

**University of Huddersfield** | School of Computing and Engineering
Project Code: ECR_2024_17
Author: Omolola Oluyemisi Haastrup
Supervisors: Dr Quratul-ain Mahesar (main), Prof Mauro Vallati (co-supervisor)

## What this is

A Streamlit prototype implementing a four-layer Dung-style argumentation framework over
scheduled temporal plans (PDDL 2.1). It uses eight argumentation schemes (S0–S7, plus the
Plan Summary Argument S8) and nine critical questions (CQ1–CQ9) to generate contestable,
premise-level explanations of why a plan is valid or invalid, rather than a single
opaque verdict.

## Live app

[Add your Streamlit Cloud URL here once deployed]

## Running locally

```bash
pip install -r requirements.txt
streamlit run app.py
```

## Pages

| Page | What it shows |
|---|---|
| About | Overview of the framework and scheme mapping |
| Plan Overview | The scheduled plan, Gantt timeline, and PSA(P) verdict |
| Explain PSA(P) | Premise-first drill-down: pick a premise, then the specific state/action/pair/ordering, then the critical question, and see the scheme instantiated for that exact selection |
| CQ Chatbot | Scheme-first navigation: pick a scheme, then a CQ, then a specific target |
| Scheme Inspector | Inspect any scheme (S0–S8) instantiated for a specific target |
| Scenarios | Five scenarios (A–E) with injected faults, verifying PSA(P) verdicts |
| AF & Verdict | Full CQ evaluation summary and the CQ→defeating-scheme map |
| Consent / Questionnaire | Participant information sheet, consent form, and the user study questionnaire |

## Ethics

This app includes the participant information sheet, consent form, and questionnaire for
an approved user study. Ethical approval: University of Huddersfield School of Computing
and Engineering Ethics Committee.

## Note on secrets

If you enable Google Sheets logging for the questionnaire, add the credentials through
Streamlit Cloud's own secrets manager (App settings → Secrets), never as a committed file.
