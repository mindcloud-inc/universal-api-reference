# SharpAPI: Generate Job Description

Creates a job description in SharpAPI.

```
POST https://connect.mindcloud.co/v1/universal/sharpAPI/latest/actions/generate-job-description
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SharpAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sharpAPI/latest/actions/generate-job-description" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Senior Software Engineer"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sharpAPI/latest/actions/generate-job-description', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Senior Software Engineer"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Job title for the position. Example: `Senior Software Engineer`. |
| `companyName` | string | no | Company name to include in the job description. Example: `MindCloud`. |
| `minimumWorkExperience` | string | no | Minimum work experience required for the role. Example: `5 years`. |
| `minimumEducation` | string | no | Minimum education requirement for the role. Example: `Bachelor's degree`. |
| `employmentType` | string | no | Employment type for the position. Example: `full_time`. |
| `requiredSkills[]` | array<string> | no | Required skills for the position. Example: `JavaScript,TypeScript,React`. |
| `optionalSkills[]` | array<string> | no | Optional skills for the position. Example: `AWS,Docker`. |
| `country` | string | no | Country for the job posting. Example: `United States`. |
| `remote` | boolean | no | Whether the role is remote. |
| `visaSponsored` | boolean | no | Whether visa sponsorship is available. |
| `language` | string | no | Language for the generated job description. Default: `English`. Example: `English`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "job_id": "string",
      "status_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `job_id` | string | SharpAPI job identifier. |
| `status_url` | string | Job status URL returned by SharpAPI. |

## Native endpoint

Through the native SharpAPI API, this operation is `POST /hr/job_description` (base URL `https://sharpapi.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-job-description.md) for the provider-specific parameters and requirements.

