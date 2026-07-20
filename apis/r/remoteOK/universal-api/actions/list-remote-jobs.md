# Remote OK: List Remote Jobs

Retrieves remote job postings from Remote OK.

```
GET https://connect.mindcloud.co/v1/universal/remoteOK/latest/actions/list-remote-jobs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Remote OK `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/remoteOK/latest/actions/list-remote-jobs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/remoteOK/latest/actions/list-remote-jobs?${params}`, {
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
      "apply_url": "https://example.com",
      "company": "Ava Chen",
      "company_logo": "https://example.com",
      "date": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "epoch": 1,
      "id": "string",
      "location": "string",
      "logo": "https://example.com",
      "original": true,
      "position": "string",
      "salary_max": 1,
      "salary_min": 1,
      "slug": "string",
      "tags": [
        "string"
      ],
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apply_url` | string | Remote OK application URL. |
| `company` | string | Hiring company name. |
| `company_logo` | string | Company logo URL when provided. |
| `date` | date | ISO timestamp for the job posting. |
| `description` | string | Full job description HTML. |
| `epoch` | number | Unix timestamp for the job posting. |
| `id` | string | Remote OK job identifier. |
| `location` | string | Location or geographic restriction when provided. |
| `logo` | string | Logo URL when provided. |
| `original` | boolean | Whether Remote OK marks this as an original listing. |
| `position` | string | Job title. |
| `salary_max` | number | Maximum salary when provided. |
| `salary_min` | number | Minimum salary when provided. |
| `slug` | string | Remote OK job slug. |
| `tags` | array<string> | Remote OK tags attached to the job. |
| `url` | string | Canonical Remote OK job URL. |

## Native endpoint

Through the native Remote OK API, this operation is `GET /api` (base URL `https://remoteok.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-remote-jobs.md) for the provider-specific parameters and requirements.

