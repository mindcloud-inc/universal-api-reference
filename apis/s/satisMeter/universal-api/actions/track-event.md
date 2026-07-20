# SatisMeter: Track Event



```
POST https://connect.mindcloud.co/v1/universal/satisMeter/latest/actions/track-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SatisMeter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/satisMeter/latest/actions/track-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "event": "user_signed_in",
  "project": "61fce0adea447e24ec27d606",
  "userId": "1234"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/satisMeter/latest/actions/track-event', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "event": "user_signed_in",
    "project": "61fce0adea447e24ec27d606",
    "userId": "1234"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `event` | string | yes | Event name. Example: `user_signed_in`. |
| `project` | string | yes | Project ID. Example: `61fce0adea447e24ec27d606`. |
| `userId` | string | yes | User ID used on your end to uniquely identify the user. Example: `1234`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native SatisMeter API returns.

## Native endpoint

Through the native SatisMeter API, this operation is `POST /api/users` (base URL `https://app.satismeter.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/track-event.md) for the provider-specific parameters and requirements.

