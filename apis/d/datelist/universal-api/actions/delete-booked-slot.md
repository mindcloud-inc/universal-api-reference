# Datelist: Delete Booked Slot

Cancels an existing booked slot in Datelist.

```
DELETE https://connect.mindcloud.co/v1/universal/datelist/latest/actions/delete-booked-slot
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Datelist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/datelist/latest/actions/delete-booked-slot?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/datelist/latest/actions/delete-booked-slot?${params}`, {
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
| `id` | number | yes | The ID of the booked slot to delete. |
| `sendEmailOnDelete` | boolean | no | Whether Datelist should send an email when the booked slot is deleted. |

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

Through the native Datelist API, this operation is `DELETE /booked_slots/:id` (base URL `https://datelist.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-booked-slot.md) for the provider-specific parameters and requirements.

