# Exa: Get Monitor Run

Retrieves a monitor run from Exa.

```
GET https://connect.mindcloud.co/v1/universal/exa/latest/actions/get-monitor-run
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Exa `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/exa/latest/actions/get-monitor-run?connectionId=$CONNECTION_ID&id=string&runId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string",
  "runId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/exa/latest/actions/get-monitor-run?${params}`, {
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
| `id` | string | yes | Monitor identifier. |
| `runId` | string | yes | Run identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cancelledAt": "2026-05-07T12:00:00.000Z",
      "completedAt": "2026-05-07T12:00:00.000Z",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "durationMs": 1,
      "failedAt": "2026-05-07T12:00:00.000Z",
      "failReason": "string",
      "id": "string",
      "monitorId": "string",
      "output": {},
      "startedAt": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cancelledAt` | date | Run cancellation timestamp. |
| `completedAt` | date | Run completion timestamp. |
| `createdAt` | date | Creation timestamp. |
| `durationMs` | number | Run duration in milliseconds. |
| `failedAt` | date | Run failure timestamp. |
| `failReason` | string | Reason the run failed. |
| `id` | string | Unique run identifier. |
| `monitorId` | string | Parent monitor identifier. |
| `output` | object | Run output payload. |
| `startedAt` | date | Run start timestamp. |
| `status` | string | Run status. |
| `updatedAt` | date | Last update timestamp. |

## Native endpoint

Through the native Exa API, this operation is `GET /monitors/:id/runs/:runId` (base URL `https://api.exa.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-monitor-run.md) for the provider-specific parameters and requirements.

