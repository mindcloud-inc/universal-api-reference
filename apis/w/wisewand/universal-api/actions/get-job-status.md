# Wisewand: Get job status

Retrieves a job status from your Wisewand workspace.

```
GET https://connect.mindcloud.co/v1/universal/wisewand/latest/actions/get-job-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wisewand `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wisewand/latest/actions/get-job-status?connectionId=$CONNECTION_ID&id=test-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "test-id"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wisewand/latest/actions/get-job-status?${params}`, {
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
| `id` | string | yes | The job ID Default: `test-id`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "completed_at": "string",
      "created_at": "string",
      "error": "string",
      "id": "string",
      "logs": "string",
      "name": "Ava Chen",
      "result": "string",
      "status": "string",
      "step": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `completed_at` | string |  |
| `created_at` | string |  |
| `error` | string |  |
| `id` | string |  |
| `logs` | string |  |
| `name` | string |  |
| `result` | string |  |
| `status` | string |  |
| `step` | string |  |

## Native endpoint

Through the native Wisewand API, this operation is `GET /v1/jobs/:id` (base URL `https://api.wisewand.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-job-status.md) for the provider-specific parameters and requirements.

