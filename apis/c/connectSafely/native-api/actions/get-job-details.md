# Get job details with ConnectSafely

Retrieve a job posting: its top card (title, company, location, pills, applicant count, hiring status) and its full description. Use the jobId from search results, or any jobId — the endpoint does not need a prior search.

`postedOn` is not returned. LinkedIn shows the posting's age rather than a date, so `postedText` carries it verbatim ("2 weeks ago").

## Endpoint

- **Method:** `POST`
- **Path:** `/search/jobs/details`
- **Base URL:** `https://api.connectsafely.ai/linkedin`
- **Official documentation:** [Get job details](https://connectsafely.ai/docs/api/linkedin-search/post-search-jobs-details-get-job-details)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | body | `string` | no | LinkedIn account ID to use. If not provided, uses the default account. |
| `jobId` | body | `string` | yes | LinkedIn job ID from search results |

## Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | `boolean` |  |
| `jobId` | `string` | LinkedIn job ID |
| `title` | `string` | Job title |
| `companyName` | `string` | Hiring company |
| `companyLogo` | `string` | Company logo URL |
| `location` | `string` | Job location, without the workplace suffix |
| `workplaceType` | `list` | Workplace pill. Absent when LinkedIn shows none. |
| `employmentType` | `string` | Employment pill as LinkedIn labels it: "Full-time", "Internship", "Contract"… |
| `postedText` | `string` | How long ago the job was posted, as LinkedIn words it ("2 weeks ago") |
| `applicantsText` | `string` | The applicant metric LinkedIn chose to show, verbatim — it varies per posting ("100 applicants", "Over 100 people clicked apply") |
| `hiringStatus` | `string` | Hiring-team signal under the applicant count ("Actively reviewing applicants", "Responses managed off LinkedIn") |
| `promoted` | `boolean` | True when the posting is promoted by the hirer |
| `verified` | `boolean` | True when LinkedIn shows its "Verified job" shield |
| `easyApply` | `boolean` | True when the application is completed on LinkedIn rather than the company site |
| `description` | `string` | Full job description with requirements and responsibilities |
| `jobUrl` | `string` | Direct URL to the job posting |
| `linkedinUrl` | `string` | Direct URL to the job posting (same as `jobUrl`) |

### Example response

```json
{
  "success": true,
  "jobId": "4445130437",
  "title": "Demand Generation Executive",
  "companyName": "BeFiSc",
  "companyLogo": "https://media.licdn.com/dms/image/v2/D560BAQF0ZsoNx5Jm4A/company-logo_100_100/...",
  "location": "Delhi, India",
  "workplaceType": "On-site",
  "employmentType": "Internship",
  "postedText": "2 weeks ago",
  "applicantsText": "100 applicants",
  "hiringStatus": "Actively reviewing applicants",
  "promoted": true,
  "verified": true,
  "easyApply": true,
  "description": "What you will do \u2022 Execute high velocity outbound prospecting...",
  "jobUrl": "https://www.linkedin.com/jobs/view/4445130437/",
  "linkedinUrl": "https://www.linkedin.com/jobs/view/4445130437/"
}
```

## Error status codes

`400`, `401`, `404`, `500`. Bodies follow the shared `{ success, code, message }` error shape.
