# Superglue: List Runs

Retrieves runs from Superglue.

```
GET https://connect.mindcloud.co/v1/universal/superglue/latest/actions/list-runs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Superglue `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/superglue/latest/actions/list-runs?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/superglue/latest/actions/list-runs?${params}`, {
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
| `toolId` | string | no | Filter runs by tool ID. Example: `stock-email-alert`. |
| `status` | list | no | Filter runs by status. One of: `aborted`, `failed`, `running`, `success`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `requestSources` | string | no | Filter by comma-separated request sources. Example: `api,webhook`. |
| `userId` | string | no | Filter runs by user ID. |
| `systemId` | string | no | Filter runs by system ID. |

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

Through the native Superglue API, this operation is `GET /runs` (base URL `https://api.superglue.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-runs.md) for the provider-specific parameters and requirements.

