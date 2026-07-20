# Anchor: Get Task Run Status

Retrieves task run status from Anchor.

```
GET https://connect.mindcloud.co/v1/universal/anchor/latest/actions/get-task-run-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Anchor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/anchor/latest/actions/get-task-run-status?connectionId=$CONNECTION_ID&runId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "runId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/anchor/latest/actions/get-task-run-status?${params}`, {
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
| `runId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "error": "string",
      "result": {},
      "run_id": "string",
      "session_id": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `error` | string |  |
| `result` | object |  |
| `run_id` | string |  |
| `session_id` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Anchor API, this operation is `GET /v2/tasks/runs/:runId/status` (base URL `https://api.anchorbrowser.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-task-run-status.md) for the provider-specific parameters and requirements.

