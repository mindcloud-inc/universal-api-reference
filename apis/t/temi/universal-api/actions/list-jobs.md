# Temi: List Jobs

Retrieves transcription jobs from Temi.

```
GET https://connect.mindcloud.co/v1/universal/temi/latest/actions/list-jobs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Temi `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/temi/latest/actions/list-jobs?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/temi/latest/actions/list-jobs?${params}`, {
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
      "callback_url": "https://example.com",
      "created_on": "2026-05-07T12:00:00.000Z",
      "duration_seconds": 1,
      "failure": "string",
      "failure_detail": "string",
      "id": "string",
      "last_modified_on": "2026-05-07T12:00:00.000Z",
      "metadata": "string",
      "name": "Ava Chen",
      "status": "string",
      "web_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `callback_url` | string | Callback URL configured for the job. |
| `created_on` | date | Job creation timestamp. |
| `duration_seconds` | number | Media duration in seconds. |
| `failure` | string | Failure reason when the job fails. |
| `failure_detail` | string | Human-readable failure detail. |
| `id` | string | Temi job ID. |
| `last_modified_on` | date | Last editor modification timestamp. |
| `metadata` | string | Metadata associated with the job. |
| `name` | string | Submitted file name. |
| `status` | string | Current job status. |
| `web_url` | string | Temi editor URL. |

## Native endpoint

Through the native Temi API, this operation is `GET /jobs` (base URL `https://api.temi.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-jobs.md) for the provider-specific parameters and requirements.

