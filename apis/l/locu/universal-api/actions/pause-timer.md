# Locu: Pause Timer

Updates the Locu timer by pausing it.

```
PUT https://connect.mindcloud.co/v1/universal/locu/latest/actions/pause-timer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Locu `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/locu/latest/actions/pause-timer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/locu/latest/actions/pause-timer', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "currentTaskId": "string",
      "duration": 1,
      "startedAt": "2026-05-07T12:00:00.000Z",
      "state": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currentTaskId` | string |  |
| `duration` | number |  |
| `startedAt` | date |  |
| `state` | string |  |

## Native endpoint

Through the native Locu API, this operation is `POST /timer/pause` (base URL `https://api.locu.app/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/pause-timer.md) for the provider-specific parameters and requirements.

