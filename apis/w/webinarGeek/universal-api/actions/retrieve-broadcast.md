# WebinarGeek: Retrieve Broadcast



```
GET https://connect.mindcloud.co/v1/universal/webinarGeek/latest/actions/retrieve-broadcast
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WebinarGeek `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webinarGeek/latest/actions/retrieve-broadcast?connectionId=$CONNECTION_ID&broadcastId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "broadcastId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webinarGeek/latest/actions/retrieve-broadcast?${params}`, {
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
| `broadcastId` | number | yes | ID of the broadcast to retrieve |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cancelled": true,
      "date": 1,
      "hasEnded": true,
      "id": 1,
      "publicReplayLink": "https://example.com",
      "replayAvailable": true,
      "startedAt": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cancelled` | boolean |  |
| `date` | number |  |
| `hasEnded` | boolean |  |
| `id` | number |  |
| `publicReplayLink` | string |  |
| `replayAvailable` | boolean |  |
| `startedAt` | number |  |

## Native endpoint

Through the native WebinarGeek API, this operation is `GET /broadcasts/:broadcastId` (base URL `https://app.webinargeek.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-broadcast.md) for the provider-specific parameters and requirements.

