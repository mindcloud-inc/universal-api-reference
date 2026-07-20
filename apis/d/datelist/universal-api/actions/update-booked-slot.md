# Datelist: Update Booked Slot

Updates an existing booked slot in Datelist.

```
PUT https://connect.mindcloud.co/v1/universal/datelist/latest/actions/update-booked-slot
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Datelist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/datelist/latest/actions/update-booked-slot" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/datelist/latest/actions/update-booked-slot', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | The ID of the booked slot to update. |
| `body` | object | no | Booked slot fields to update, using the documented booked-slot object shape. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "calendarId": 1,
      "createdAt": "string",
      "createdFrom": "string",
      "customFieldValues": {},
      "deletedAt": "string",
      "email": "ava@example.com",
      "emailNotificationReallySentAt": "ava@example.com",
      "emailNotificationSentAt": "ava@example.com",
      "end": "string",
      "externalId": "string",
      "firstName": "Ava",
      "id": 1,
      "integrationDetails": {},
      "language": "string",
      "lastName": "Chen",
      "phone": "string",
      "phoneNotificationReallySentAt": "string",
      "phoneNotificationSentAt": "string",
      "productId": 1,
      "start": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `calendarId` | number | Calendar ID. |
| `createdAt` | string | Creation timestamp. |
| `createdFrom` | string | Source that created the booking. |
| `customFieldValues` | object | Custom field values. |
| `deletedAt` | string | Deletion timestamp, when present. |
| `email` | string | Customer email. |
| `emailNotificationReallySentAt` | string | Confirmed email send timestamp. |
| `emailNotificationSentAt` | string | Email notification sent timestamp. |
| `end` | string | End timestamp. |
| `externalId` | string | External identifier. |
| `firstName` | string | Customer first name. |
| `id` | number | Booked slot ID. |
| `integrationDetails` | object | Integration details. |
| `language` | string | Preferred language. |
| `lastName` | string | Customer last name. |
| `phone` | string | Customer phone. |
| `phoneNotificationReallySentAt` | string | Confirmed phone send timestamp. |
| `phoneNotificationSentAt` | string | Phone notification sent timestamp. |
| `productId` | number | Product ID. |
| `start` | string | Start timestamp. |
| `updatedAt` | string | Update timestamp. |

## Native endpoint

Through the native Datelist API, this operation is `PATCH /booked_slots/:id` (base URL `https://datelist.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-booked-slot.md) for the provider-specific parameters and requirements.

