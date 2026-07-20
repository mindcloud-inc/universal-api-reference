# Locu: Start Timer

Starts a new session timer in Locu.

```
POST https://connect.mindcloud.co/v1/universal/locu/latest/actions/start-timer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Locu `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/locu/latest/actions/start-timer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "duration": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/locu/latest/actions/start-timer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "duration": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `duration` | number | yes | Timer duration in seconds. Must be a positive integer. |
| `taskId` | string | no | Optional task ID to start working on. |

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

Through the native Locu API, this operation is `POST /timer/start` (base URL `https://api.locu.app/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/start-timer.md) for the provider-specific parameters and requirements.

