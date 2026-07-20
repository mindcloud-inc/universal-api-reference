# OnceHub: Set Booking No-Show



```
PUT https://connect.mindcloud.co/v1/universal/onceHub/latest/actions/set-booking-no-show
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OnceHub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/onceHub/latest/actions/set-booking-no-show" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/onceHub/latest/actions/set-booking-no-show', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The OnceHub booking identifier. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native OnceHub API returns.

## Native endpoint

Through the native OnceHub API, this operation is `POST /v2/bookings/:id/no-show` (base URL `https://api.oncehub.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-booking-no-show.md) for the provider-specific parameters and requirements.

