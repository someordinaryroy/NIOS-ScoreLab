# NIOS-ScoreLab

**An offline marksheet and passing-marks calculator for NIOS Class 10 and Class 12 students.**

NIOS ScoreLab is a lightweight, browser-based application designed to help National Institute of Open Schooling (NIOS) Stream 1 learners estimate their examination results, understand subject-wise passing requirements and plan their preparation targets.

Built with plain HTML, CSS and JavaScript, ScoreLab runs entirely on your device without a server, internet connection or external dependencies.

## Features

- **Class 10 and Class 12 support** — switch between Secondary and Senior Secondary courses directly from the header.
- **Subject-wise calculations** — 40 Class 10 and 47 Class 12 confirmed subject presets, with manual configuration for six additional Class 12 entries and allocation overrides for older syllabi.
- **Automatic mark conversion** — enter raw theory marks, Tutor Marked Assignment (TMA) marks and practical marks to estimate your final marksheet score.
- **Passing-marks analysis** — separate class-specific rules, aggregate checks and borderline-result warnings.
- **Exam target calculator** — estimate the raw theory marks needed to pass or achieve a desired subject score.
- **Marksheet summary** — view total marks, average percentage and subject-wise results for up to seven subjects.
- **Certification check** — estimates whether a qualifying five-subject marks combination exists, including language requirements.
- **Offline storage** — separate saved workspaces for Class 10 and Class 12, where browser storage is supported.
- **Export options** — download results as CSV or print/save as PDF using your browser.
- **Responsive interface** — clean layouts for desktop and mobile, with light and dark modes.

## Getting started

1. Download `NIOS_ScoreLab_Offline_v2.html` from this repository.
2. Open the file in a modern web browser, such as Firefox, Chrome or Edge.
3. Select **Class 10** or **Class 12** from the header.
4. Choose your subjects and enter your expected or actual marks.
5. Review the estimated marksheet, passing status and required theory marks.

No installation, package manager, build process or local server is required.

### TMA input formats

| Mode | When to use it |
| --- | --- |
| Portal TMA score | Your TMA marks are displayed out of 20. |
| Already weighted TMA score | You have the TMA marks already converted to the subject's marksheet weightage. |

Enter the **total practical marks**, including formative and summative components where applicable. Do not enter only the final practical examination score if other practical assessment marks are required.

## How calculations work

Under the standard Stream 1 TMA scheme, let `T` be the maximum raw theory marks of a 100-mark subject. The remaining `100 - T` marks are allocated to practical assessment.

```text
Weighted theory = Raw theory marks × 0.80
Weighted TMA   = (Portal TMA marks / 20) × (T × 0.20)
Estimated total = Weighted theory + Weighted TMA + Practical marks
```

When using already weighted TMA mode, the entered TMA score is added directly without further conversion.

### Example: Psychology (328)

| Component | Marks |
| --- | ---: |
| Raw theory | 45/100 |
| Weighted theory | 36/80 |
| TMA | 20/20 |
| Practical | Not applicable |
| **Estimated final score** | **56/100** |

## Passing criteria

| Requirement | Class 10 | Class 12 |
| --- | --- | --- |
| External examination | At least 33% in combined weighted theory and practical marks, excluding TMA | At least 33% separately in theory and practical, wherever applicable, excluding TMA |
| Subject aggregate | At least 33/100 under the calculator's standard academic model | At least 33/100 under the calculator's standard academic model |
| Separate TMA pass requirement | None | None |
| Qualifying subject combination | At least five passing subjects, including one or two languages | At least five passing subjects, including one or two languages |

ScoreLab uses unrounded calculations and conservative whole-mark planning targets. Near-threshold results are flagged for verification rather than presented as guaranteed passes.

## Technology stack

| Technology | Purpose |
| --- | --- |
| HTML5 | Application structure and form controls |
| CSS3 | Responsive layout, styling and themes |
| Vanilla JavaScript | Calculations, validation and application state |
| Web Storage API | Local saving, where supported |
| Blob API | CSV export |

There are no external libraries, CDNs, accounts or backend services required for the calculator to operate.

## Privacy

Marks and preferences are processed locally in the browser. The application does not send them to a remote server. Local storage may be unavailable or cleared depending on browser settings; export your results if you want to keep a separate copy.

## Official references

The subject allocations and calculation model are based on the following NIOS resources:

- [NIOS Academic Prospectus 2026–27](https://cdn.nios.ac.in/cms/documents/2026/Oct/18/1792322980_Academic_Prospectus_2026-27.pdf) — subject lists, marks allocations and certification requirements (Tables 8–9).
- [NIOS Examination Bye-laws](https://cdn.nios.ac.in/cms/documents/2021/Dec/27/Bye_laws_Governing_Examinations_Certification_2012_amended_08122021.pdf) — passing and certification criteria (Section 3.5).
- [NIOS Internal Assessment Notification](https://cdn.nios.ac.in/cms/documents/2020/Oct/20/TMANoti2014.pdf) — internal assessment and theory weightage.
- [NIOS Regional Centre Pune FAQs](https://rcpune.nios.ac.in/faqs.html).

Reference baseline: 25 November 2026. The calculator is not restricted to a particular examination season, but the applicable syllabus and rules should be checked for each session.

## Limitations and disclaimer

NIOS ScoreLab is an independent, unofficial educational utility. It is not affiliated with or endorsed by NIOS.

- Designed for **Stream 1** learners using the standard 100-mark academic subject and TMA model.
- Official rounding, moderation, absence, revised syllabi and subject-specific rules may affect actual results.
- Six additional Class 12 entries require manually verified marks allocations.
- Separate vocational certification schemes, Transfer of Credit (TOC) and other special arrangements are not modelled.
- The certification indicator checks marks and language combinations only, not administrative eligibility or mandatory time-gap requirements.

Always refer to the official NIOS marksheet and applicable examination rules for the final result.

## Feedback and contributions

Suggestions for improvements, accessibility fixes, bug reports and corrections to subject allocations are welcome through GitHub Issues or pull requests. When reporting a calculation issue, include the class, subject code, entered marks, expected outcome and an official reference where available. Avoid sharing personal details or enrollment numbers.

---

**NIOS-ScoreLab — Understand your marks. Plan your preparation.**
