# Jobicy: List Remote Jobs by Region



```
GET https://connect.mindcloud.co/v1/universal/jobicy/latest/actions/list-remote-jobs-by-region
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jobicy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jobicy/latest/actions/list-remote-jobs-by-region?connectionId=$CONNECTION_ID&geo=usa" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "geo": "usa"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jobicy/latest/actions/list-remote-jobs-by-region?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `geo` | string | yes | Jobicy region slug such as usa, canada, europe, latam, apac, uk, germany, australia, or brazil. Example: `usa`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "companyLogo": "string",
      "companyName": "Ava Chen",
      "id": 1,
      "jobDescription": "string",
      "jobExcerpt": "string",
      "jobGeo": "string",
      "jobIndustry": [
        "string"
      ],
      "jobLevel": "string",
      "jobSlug": "string",
      "jobTitle": "string",
      "jobType": [
        "string"
      ],
      "pubDate": "2026-05-07T12:00:00.000Z",
      "salaryCurrency": "string",
      "salaryMax": 1,
      "salaryMin": 1,
      "salaryPeriod": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companyLogo` | string | Company logo image URL. |
| `companyName` | string | Company name. |
| `id` | number | Jobicy job identifier. |
| `jobDescription` | string | Full HTML job description. |
| `jobExcerpt` | string | Short job summary excerpt. |
| `jobGeo` | string | Geographic restriction or region. |
| `jobIndustry` | array<string> | Jobicy job categories attached to the listing. |
| `jobLevel` | string | Experience level label. |
| `jobSlug` | string | Jobicy slug for the job listing. |
| `jobTitle` | string | Job title. |
| `jobType` | array<string> | Job type labels such as Full-Time or Contract. |
| `pubDate` | date | Job publication timestamp. |
| `salaryCurrency` | string | ISO 4217 salary currency code when available. |
| `salaryMax` | number | Maximum salary when Jobicy provides it. |
| `salaryMin` | number | Minimum salary when Jobicy provides it. |
| `salaryPeriod` | string | Salary period when available, such as yearly. |
| `url` | string | Canonical Jobicy job URL. |

## Native endpoint

Through the native Jobicy API, this operation is `GET /remote-jobs` (base URL `https://jobicy.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-remote-jobs-by-region.md) for the provider-specific parameters and requirements.

