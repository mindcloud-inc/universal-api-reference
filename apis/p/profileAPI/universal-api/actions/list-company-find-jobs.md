# profileAPI: List Company Find Jobs

Retrieves company search jobs from profileAPI.

```
GET https://connect.mindcloud.co/v1/universal/profileAPI/latest/actions/list-company-find-jobs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a profileAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/profileAPI/latest/actions/list-company-find-jobs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/profileAPI/latest/actions/list-company-find-jobs?${params}`, {
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
| `status` | string | no | Optional job status filter. Current docs state list jobs supports filtering by status. Example: `completed`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "error": {
        "code": 1,
        "message": "string"
      },
      "jobId": "string",
      "progress": 1,
      "requestedAt": "2026-05-07T12:00:00.000Z",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `error.code` | number |  |
| `error.message` | string |  |
| `jobId` | string |  |
| `progress` | number |  |
| `requestedAt` | date |  |
| `status` | string |  |

## Native endpoint

Through the native profileAPI API, this operation is `GET /companies/find/jobs` (base URL `https://api.profileapi.com/2024-03-01`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-company-find-jobs.md) for the provider-specific parameters and requirements.

