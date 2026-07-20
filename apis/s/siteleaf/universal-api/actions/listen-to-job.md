# Siteleaf: Listen to Job

Retrieves a job status stream from Siteleaf.

```
GET https://connect.mindcloud.co/v1/universal/siteleaf/latest/actions/listen-to-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Siteleaf `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/siteleaf/latest/actions/listen-to-job?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/siteleaf/latest/actions/listen-to-job?${params}`, {
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
| `jobId` | string | no | Siteleaf job identifier |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Siteleaf API returns.

## Native endpoint

Through the native Siteleaf API, this operation is `GET /jobs/:job_id` (base URL `https://api.siteleaf.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/listen-to-job.md) for the provider-specific parameters and requirements.

