# Skyvern: Cancel Run

Cancels a task or workflow run in Skyvern.

```
PUT https://connect.mindcloud.co/v1/universal/skyvern/latest/actions/cancel-run
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Skyvern `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/skyvern/latest/actions/cancel-run" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "runId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/skyvern/latest/actions/cancel-run', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "runId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `runId` | string | yes | The task run or workflow run ID to cancel. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Skyvern API returns.

## Native endpoint

Through the native Skyvern API, this operation is `POST /v1/runs/:run_id/cancel` (base URL `https://api.skyvern.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-run.md) for the provider-specific parameters and requirements.

