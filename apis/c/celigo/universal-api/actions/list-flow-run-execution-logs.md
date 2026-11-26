# Celigo: List Flow Run Execution Logs



```
GET https://connect.mindcloud.co/v1/universal/celigo/latest/actions/list-flow-run-execution-logs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Celigo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/celigo/latest/actions/list-flow-run-execution-logs?connectionId=$CONNECTION_ID&flowId=string&jobId=6798e7a330f8f5fb4c2ee2fb" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "flowId": "string",
  "jobId": "6798e7a330f8f5fb4c2ee2fb"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/celigo/latest/actions/list-flow-run-execution-logs?${params}`, {
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
| `flowId` | list<string> | yes | Flow that ran. |
| `jobId` | string | yes | Flow-run job ID (a job of type Flow). Example: `6798e7a330f8f5fb4c2ee2fb`. |
| `status` | list<string> | no | Only return entries with this record outcome. One of: `error`, `ignore`, `success`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `expOrImpId[]` | array<string> | no | Only return entries produced by these export or import steps. Accepts multiple values in one string, delimited by `,`. |
| `traceKeyPrefix` | string | no | Only return entries whose trace key starts with this value. |
| `sortOrder` | list<string> | no | Order by start time. Defaults to newest first. One of: `asc`, `desc`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Celigo API returns.

## Native endpoint

Through the native Celigo API, this operation is `GET /flows/:flowId/jobs/:jobId/logs` (base URL `https://{{credentials.apiHost}}/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-flow-run-execution-logs.md) for the provider-specific parameters and requirements.

