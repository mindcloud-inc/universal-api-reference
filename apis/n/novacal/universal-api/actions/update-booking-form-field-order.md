# Novacal: Update Booking Form Field Order

Updates booking form field order in Novacal.

```
PUT https://connect.mindcloud.co/v1/universal/novacal/latest/actions/update-booking-form-field-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Novacal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/novacal/latest/actions/update-booking-form-field-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/novacal/latest/actions/update-booking-form-field-order', {
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
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Reorder status message. |
| `success` | boolean | Whether the reorder request succeeded. |

## Native endpoint

Through the native Novacal API, this operation is `PUT /v1/event-types/:eventType/booking-forms/update-order` (base URL `https://api.novacal.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-booking-form-field-order.md) for the provider-specific parameters and requirements.

