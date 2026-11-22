# Job Application Tailoring Agent

A Python project that matches a job description against a candidate profile and generates a tailored CV and cover letter. It uses LangGraph to coordinate drafting, content review, and revision. The workflow pauses for human review of the Word documents before exporting them to PDF.

## Demo results

The demo uses a fictional candidate, Alex Chen, and a fictional Junior Software Engineer job advertisement.

- [Sample job matching report](examples/sample_match_report.md)
- [Sample CV](examples/sample_cv.pdf)
- [Sample cover letter](examples/sample_cover_letter.pdf)

## How it works

1. **Match the job description** against the candidate's education, projects, internships, and skills. The report cites evidence, identifies gaps, and flags eligibility details that need confirmation.
2. **Generate Word drafts.** DeepSeek returns structured content. Python fills a Word CV template and creates a separate cover letter.
3. **Review and revise.** The workflow checks draft claims against the profile and job description. It can revise drafts and adjust Word formatting, with a fixed limit on automatic revisions.
4. **Pause for human approval.** Open the latest DOCX files in Word, check the wording and pagination, and save any edits.
5. **Export to PDF.** Type `EXPORT` in the final Colab cell to convert the reviewed DOCX files. The applicant submits the documents manually.

A job ad without explicit skill criteria can receive `Skills score: N/A`. The user can still choose to generate drafts based on relevant experience and role fit.

## Run the demo in Google Colab

You need a DeepSeek API key with available API credit. The notebook prompts for the key using a hidden input. API calls may incur charges.

1. Open `job_application_agent_demo.ipynb` in Google Colab.
2. In Colab's **Files** panel, upload these three files to `/content`:
   - `sample_profile.md`
   - `sample_job_description.md`
   - `sample_cv_template.docx`
3. Run the setup and workflow cells up to the cell that starts the application.
4. Press **Enter** when asked whether to use the sample job description. After reading the match report, type `y` to generate the Word drafts.
5. Open the two DOCX files from the latest folder printed by the notebook. Review them and save any edits to the same paths.
6. While the same Colab runtime is still active, run the final export cell and type `EXPORT`. Download the PDFs from the output paths printed by the notebook.

## Repository files

| File | Purpose |
| --- | --- |
| `job_application_agent_demo.ipynb` | Colab notebook for matching, drafting, review, and export |
| `sample_profile.md` | Fictional candidate profile with evidence records |
| `sample_job_description.md` | Fictional job advertisement for the demo |
| `sample_cv_template.docx` | Word template with placeholders for the CV sections |
| `examples/` | Sample match report and final PDF documents |

## Tech stack

- **Python and LangGraph** for workflow orchestration, revision limits, and the approval pause
- **DeepSeek API** for matching, writing, and review
- **python-docx** for Word template filling and formatting
- **LibreOffice** for DOCX-to-PDF conversion

## Review scope

The automatic checks can flag unsupported claims and suggest Word formatting changes. The user verifies factual accuracy, final pagination, and document appearance before export.
