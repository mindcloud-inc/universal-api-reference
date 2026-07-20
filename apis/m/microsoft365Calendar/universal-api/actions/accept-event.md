# Microsoft 365 Calendar: Accept Event

Accepts an event invitation in Microsoft 365 Calendar.

```
PUT https://connect.mindcloud.co/v1/universal/microsoft365Calendar/latest/actions/accept-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft 365 Calendar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/microsoft365Calendar/latest/actions/accept-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "eventId": "AAMkAG..."
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoft365Calendar/latest/actions/accept-event', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "eventId": "AAMkAG..."
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `eventId` | string | yes | The ID of the Outlook event to accept. Example: `AAMkAG...`. |
| `comment` | string | no | Optional comment to include with the accept response. Example: `Accepted from MindCloud verification`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Microsoft 365 Calendar API returns.

## Native endpoint

Through the native Microsoft 365 Calendar API, this operation is `POST /v1.0/me/events/{{eventId}}/accept` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/accept-event.md) for the provider-specific parameters and requirements.

