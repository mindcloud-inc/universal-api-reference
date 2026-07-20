# Generate Job Description with SharpAPI

Creates a job description in SharpAPI.

## Endpoint

- **Method:** `POST`
- **Path:** `/hr/job_description`
- **Base URL:** `https://sharpapi.com/api/v1`
- **Official documentation:** [Generate Job Description](https://sharpapi.com/en/catalog/ai/hr-tech/job-description-generator)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Job title for the position. |
| `company_name` | body | `string` | no | Company name to include in the job description. |
| `minimum_work_experience` | body | `string` | no | Minimum work experience required for the role. |
| `minimum_education` | body | `string` | no | Minimum education requirement for the role. |
| `employment_type` | body | `string` | no | Employment type for the position. |
| `required_skills[]` | body | `array<string>` | no | Required skills for the position. |
| `optional_skills[]` | body | `array<string>` | no | Optional skills for the position. |
| `country` | body | `string` | no | Country for the job posting. |
| `remote` | body | `boolean` | no | Whether the role is remote. |
| `visa_sponsored` | body | `boolean` | no | Whether visa sponsorship is available. |
| `language` | body | `string` | no | Language for the generated job description. |
