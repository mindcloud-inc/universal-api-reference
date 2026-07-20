# Eventzilla: Confirm Event Order

Confirms an event order in Eventzilla.

```
PUT https://connect.mindcloud.co/v1/universal/eventzilla/latest/actions/confirm-event-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eventzilla `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/eventzilla/latest/actions/confirm-event-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "checkoutId": 1,
  "eventId": 1,
  "comments": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eventzilla/latest/actions/confirm-event-order', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "checkoutId": 1,
    "eventId": 1,
    "comments": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `checkoutId` | number | yes | The checkout identifier to confirm. |
| `eventId` | number | yes | The Eventzilla event identifier. |
| `comments` | string | yes | Organizer comment to store with the confirmation. |
| `sendEmail` | boolean | no | Set false to avoid sending the confirmation email. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "orderconfirm": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `orderconfirm` | string |  |

## Native endpoint

Through the native Eventzilla API, this operation is `POST /events/order/confirm` (base URL `https://www.eventzillaapi.net/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/confirm-event-order.md) for the provider-specific parameters and requirements.

