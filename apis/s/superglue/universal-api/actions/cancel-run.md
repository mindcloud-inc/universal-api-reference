# Superglue: Cancel Run

Cancels an existing run in Superglue.

```
PUT https://connect.mindcloud.co/v1/universal/superglue/latest/actions/cancel-run
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Superglue `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/superglue/latest/actions/cancel-run" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "runId": "7f3e9c1a-2b4d-4e8f-9a3b-1c5d7e9f2a4b"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/superglue/latest/actions/cancel-run', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "runId": "7f3e9c1a-2b4d-4e8f-9a3b-1c5d7e9f2a4b"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `runId` | string | yes | ID of the Superglue run to cancel. Example: `7f3e9c1a-2b4d-4e8f-9a3b-1c5d7e9f2a4b`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "error": "string",
      "executionMode": "string",
      "metadata": {
        "completedAt": "2026-05-07T12:00:00.000Z",
        "durationMs": 1,
        "startedAt": "2026-05-07T12:00:00.000Z"
      },
      "options": {},
      "requestSource": "string",
      "resultStorageUri": "string",
      "runId": "string",
      "status": "string",
      "stepResults": [
        {}
      ],
      "tool": {
        "id": "string",
        "instruction": "string",
        "name": "Ava Chen"
      },
      "toolId": "string",
      "toolPayload": {},
      "traceId": "string",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Tool-specific execution result data for synchronous runs. |
| `error` | string | Error message when the run failed or was aborted. |
| `executionMode` | string | Execution mode used for system credentials. |
| `metadata.completedAt` | date | Run completion timestamp when finished. |
| `metadata.durationMs` | number | Run duration in milliseconds. |
| `metadata.startedAt` | date | Run start timestamp. |
| `options` | object | Execution options used for this run. |
| `requestSource` | string | Source identifier for where the run was initiated. |
| `resultStorageUri` | string | Storage URI for full run results when available. |
| `runId` | string | Unique identifier for this run. |
| `status` | string | Execution status for the run. |
| `stepResults` | array<object> | Per-step execution results for multi-step tools. |
| `tool.id` | string | Identifier of the executed tool. |
| `tool.instruction` | string | Human-readable instruction for the executed tool. |
| `tool.name` | string | Name of the executed tool. |
| `toolId` | string | ID of the tool that was executed. |
| `toolPayload` | object | Inputs provided when running the tool. |
| `traceId` | string | Trace ID for debugging and log correlation. |
| `userId` | string | User or end user who triggered the run. |

## Native endpoint

Through the native Superglue API, this operation is `POST /runs/:runId/cancel` (base URL `https://api.superglue.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-run.md) for the provider-specific parameters and requirements.

