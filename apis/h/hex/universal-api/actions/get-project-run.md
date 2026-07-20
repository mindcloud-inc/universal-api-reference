# Hex: Get Project Run



```
GET https://connect.mindcloud.co/v1/universal/hex/latest/actions/get-project-run
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hex `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hex/latest/actions/get-project-run?connectionId=$CONNECTION_ID&projectId=string&runId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string",
  "runId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hex/latest/actions/get-project-run?${params}`, {
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
| `projectId` | string | yes | Unique ID for a Hex project. |
| `runId` | string | yes | Unique ID for a Hex project run. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "elapsedTime": 1,
      "endTime": "2026-05-07T12:00:00.000Z",
      "flagConfigOverride": "string",
      "notifications": [
        {}
      ],
      "projectId": "string",
      "projectVersion": 1,
      "runId": "string",
      "runUrl": "https://example.com",
      "startTime": "2026-05-07T12:00:00.000Z",
      "stateEvents": [
        {}
      ],
      "status": "string",
      "traceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `elapsedTime` | number |  |
| `endTime` | date |  |
| `flagConfigOverride` | string |  |
| `notifications` | array<object> |  |
| `projectId` | string |  |
| `projectVersion` | number |  |
| `runId` | string |  |
| `runUrl` | string |  |
| `startTime` | date |  |
| `stateEvents` | array<object> |  |
| `status` | string |  |
| `traceId` | string |  |

## Native endpoint

Through the native Hex API, this operation is `GET /projects/:projectId/runs/:runId` (base URL `https://app.hex.tech/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project-run.md) for the provider-specific parameters and requirements.

