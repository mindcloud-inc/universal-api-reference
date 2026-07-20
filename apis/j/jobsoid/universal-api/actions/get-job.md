# Jobsoid: Get job

Retrieves a published job from Jobsoid.

```
GET https://connect.mindcloud.co/v1/universal/jobsoid/latest/actions/get-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jobsoid `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jobsoid/latest/actions/get-job?connectionId=$CONNECTION_ID&jobId=130458" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "130458"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jobsoid/latest/actions/get-job?${params}`, {
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
| `jobId` | number | yes | Unique Jobsoid job identifier from the jobs feed. Example: `130458`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "applyUrl": "https://example.com",
      "attributes": [
        {}
      ],
      "closingDate": "2026-05-07T12:00:00.000Z",
      "code": "string",
      "company": "string",
      "department": {},
      "description": "string",
      "division": [
        {}
      ],
      "experience": "string",
      "function": {},
      "hostedUrl": "https://example.com",
      "id": 1,
      "industry": "string",
      "location": {},
      "positions": 1,
      "postedDate": "2026-05-07T12:00:00.000Z",
      "salary": "string",
      "slug": "string",
      "title": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `applyUrl` | string |  |
| `attributes` | array<object> |  |
| `closingDate` | date |  |
| `code` | string |  |
| `company` | string |  |
| `department` | object |  |
| `description` | string |  |
| `division` | array<object> |  |
| `experience` | string |  |
| `function` | object |  |
| `hostedUrl` | string |  |
| `id` | number |  |
| `industry` | string |  |
| `location` | object |  |
| `positions` | number |  |
| `postedDate` | date |  |
| `salary` | string |  |
| `slug` | string |  |
| `title` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Jobsoid API, this operation is `GET /api/v1/jobs/{{jobId}}` (base URL `https://demo.jobsoid.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-job.md) for the provider-specific parameters and requirements.

