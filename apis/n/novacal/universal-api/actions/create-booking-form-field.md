# Novacal: Create Booking Form Field

Creates a new booking form field in Novacal.

```
POST https://connect.mindcloud.co/v1/universal/novacal/latest/actions/create-booking-form-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Novacal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/novacal/latest/actions/create-booking-form-field" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/novacal/latest/actions/create-booking-form-field', {
  method: 'POST',
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
      "id": 1,
      "identifier": "string",
      "is_active": true,
      "is_required": true,
      "label": "string",
      "position": 1,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number | Booking form field ID. |
| `identifier` | string | Field identifier. |
| `is_active` | boolean | Whether the field is active. |
| `is_required` | boolean | Whether the field is required. |
| `label` | string | Field label. |
| `position` | number | Field display position. |
| `type` | string | Field type. |

## Native endpoint

Through the native Novacal API, this operation is `POST /v1/event-types/:eventType/booking-forms` (base URL `https://api.novacal.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-booking-form-field.md) for the provider-specific parameters and requirements.

