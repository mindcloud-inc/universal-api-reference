# Ubidots: Get Event Log



```
GET https://connect.mindcloud.co/v1/universal/ubidots/latest/actions/get-event-log
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ubidots `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ubidots/latest/actions/get-event-log?connectionId=$CONNECTION_ID&eventKey=string&logId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "eventKey": "string",
  "logId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ubidots/latest/actions/get-event-log?${params}`, {
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
| `eventKey` | string | yes | The event ID or key. |
| `logId` | string | yes | The event log ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "event": {},
      "id": "string",
      "message": "string",
      "status": "string",
      "value": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `event` | object |  |
| `id` | string |  |
| `message` | string |  |
| `status` | string |  |
| `value` | object |  |

## Native endpoint

Through the native Ubidots API, this operation is `GET /events/:event_key/logs/:log_id/` (base URL `https://industrial.api.ubidots.com/api/v2.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-event-log.md) for the provider-specific parameters and requirements.

