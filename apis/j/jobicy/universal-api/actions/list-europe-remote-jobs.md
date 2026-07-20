# Jobicy: List Europe Remote Jobs



```
GET https://connect.mindcloud.co/v1/universal/jobicy/latest/actions/list-europe-remote-jobs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jobicy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jobicy/latest/actions/list-europe-remote-jobs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jobicy/latest/actions/list-europe-remote-jobs?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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
| `companyLogo` | string |  |
| `companyName` | string |  |
| `id` | number |  |
| `jobDescription` | string |  |
| `jobExcerpt` | string |  |
| `jobGeo` | string |  |
| `jobIndustry` | array<string> |  |
| `jobLevel` | string |  |
| `jobSlug` | string |  |
| `jobTitle` | string |  |
| `jobType` | array<string> |  |
| `pubDate` | date |  |
| `salaryCurrency` | string |  |
| `salaryMax` | number |  |
| `salaryMin` | number |  |
| `salaryPeriod` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Jobicy API, this operation is `GET /remote-jobs` (base URL `https://jobicy.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-europe-remote-jobs.md) for the provider-specific parameters and requirements.

