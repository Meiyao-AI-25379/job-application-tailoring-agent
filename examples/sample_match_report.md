# Job Application Matching Report

## Eligibility and Availability

The ad states four explicit conditions/commitments. The profile does not cover dates, start dates, or availability.

- **Full Australian working rights** — Ad: "Full Australian working rights." Status: **Needs confirmation.** The profile excerpt gives no citizenship, visa, or work-rights information. This is absent, not inferred.
- **Full-time employment** — Ad: "Employment type: Full time." Status: **Needs confirmation.** No availability or hours information is supplied for the candidate.
- **Start date / availability** — Not stated in the ad. No interview month or commencement date is given, so no timing commitment can be assessed against.
- **Location / hybrid (Melbourne, VIC)** — Ad: "Location: Melbourne, VIC (Hybrid)." Status: **Needs confirmation.** The profile does not state the candidate's location or willingness to work in Melbourne.

No other participation commitments (e.g. training period, mandatory licences) appear in the ad.

## Skills and Experience Match

Skills score: 72/100

The ad separates duties from selection criteria. Duties (implementing/testing API endpoints, maintaining SQL, documenting changes) underpin the **Required** list below; only the explicitly listed criteria are scored. I assess five criteria (three required, two desirable), weighting required ones by 2.

- **Python experience (Required)** — **Strong match (1).** E01 "Used Python, SQL and Git in coursework"; P02 "Built a Python command-line tool to import service requests from CSV." Meets the criterion's flexibility ("coursework, projects or work").
- **SQL with joins and aggregations (Required)** — **Strong match (1).** P03 "Wrote queries with joins and aggregations to report weekly booking activity."
- **Testing changes and documenting reproduction/verification (Required)** — **Partial match (0.5).** P02 "Wrote unit tests for the import logic and documented how to run them"; W02 "Documented the handover process for incoming interns." Testing is coursework/individual-project context and documentation is administrative, so it partly matches "testing software changes and documenting how to reproduce or verify them" rather than fully.
- **REST APIs with FastAPI or similar (Desirable)** — **Strong match (1).** P01 "Implemented FastAPI endpoints to add, update and retrieve stock records."
- **Git and code review (Desirable)** — **Partial match (0.5).** E01 "Used Python, SQL and Git in coursework." Git is evidenced; code review is not. (Delete the exposure-to-cloud criterion below if only five are counted — see note.)

Calculation (three required at weight 2, two desirable at weight 1): weighted points = (1×2)+(1×2)+(0.5×2)+(1×1)+(0.5×1) = 7.0; weights = 2+2+2+1+1 = 8; 100×7/8 = 87.5. *Correction: on the five criteria above the score is **88/100**. If a sixth desirable criterion is added, the score changes; see note.*

- **Cloud deployment exposure (Desirable)** — **No evidence found (0).** Not stated in the profile.

Including that sixth criterion: points = 7.0, weights = 9, 100×7/9 = 78 → **78/100**. Score reported for the full ad's criteria: **78/100**.

## Role Fit

- The employer seeks a junior who can "help implement and test API endpoints, maintain SQL queries and document changes." Records P01 (FastAPI endpoints, request validation) and P03 (SQL joins/aggregations) map directly to these duties; P02 (unit tests, documented run steps) supports the testing/documentation duty.
- The ad recruits someone with Python "through coursework, projects or work," signalling a training/early-career audience. E01 (Graduate Diploma in Computing, "Completed") plus P01–P03 show a completed conversion qualification and applied projects, aligning with that entry-level audience.
- A documented field change is visible: E02 (Business Analytics, Excel) and W01/W02 (operations/admin internships) precede or overlap E01, which adds computing. The chronology reads business/operations → computing study → technical projects, though exact dates are not supplied, so ordering is inferred from record sequence only. This supports a transferable, data-and-process background (W01 stock checks, E02 sales analysis) alongside technical preparation.

The candidate's own motivation for the field change is not stated; this is a documented study path, not a declared career goal.

## Experience to Prioritise

- **P01 (Inventory Tracking API):** Highlight FastAPI endpoints and Pydantic validation ("Validated request data with Pydantic and returned clear error messages"). Directly matches the desirable REST API criterion and the core API duty; good cover-letter project choice ("one project you contributed to").
- **P03 (Booking Database Design):** Emphasise joins and aggregations in SQL ("Wrote queries with joins and aggregations to report weekly booking activity") to evidence the required SQL capability.
- **P02 (Service Request Tracker):** Frame the "unit tests for the import logic" and documented run steps as testing-plus-documentation evidence, closing the partial gap.
- **E01 + W01/W02:** Present the computing qualification beside internship documentation habits ("Documented the handover process for incoming interns") to show reproducible-process documentation and transferable rigour.

## Candidate Checks

- Can you confirm full Australian working rights? The ad requires them and the profile is silent.
- Are you available for full-time work in Melbourne (hybrid), and from what date? Neither availability nor location is stated.
- Which single project best evidences testing *and* documentation together (e.g. P02), so the cover letter can address that required criterion directly?
- Is there any Git code-review or cloud-deployment exposure (desirable but unevidenced) you can substantiate?