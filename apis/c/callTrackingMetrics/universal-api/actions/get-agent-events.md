# CallTrackingMetrics: Get Agent Events

Retrieves agent event records from CallTrackingMetrics.

```
GET https://connect.mindcloud.co/v1/universal/callTrackingMetrics/latest/actions/get-agent-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CallTrackingMetrics `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/callTrackingMetrics/latest/actions/get-agent-events?connectionId=$CONNECTION_ID&limit=25&offset=0&userId=string&startTime=1&endTime=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "userId": "string",
  "startTime": "1",
  "endTime": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/callTrackingMetrics/latest/actions/get-agent-events?${params}`, {
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
| `userId` | string | yes | The internal CTM user ID for the agent whose events should be returned. |
| `startTime` | number | yes | Start of the event window in epoch seconds. |
| `endTime` | number | yes | End of the event window in epoch seconds. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "events": [
        [
          "string"
        ]
      ],
      "query": {
        "afterTime": "2026-05-07T12:00:00.000Z",
        "beforeTime": "2026-05-07T12:00:00.000Z"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `events[]` | array |  |
| `query` | object |  |
| `query.afterTime` | date |  |
| `query.beforeTime` | date |  |

## Native endpoint

Through the native CallTrackingMetrics API, this operation is `GET /accounts/:accountId/agents/events.json` (base URL `https://api.calltrackingmetrics.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-agent-events.md) for the provider-specific parameters and requirements.

