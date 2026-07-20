# Datelist: List Booked Slots

Retrieves booked slots from Datelist by email, calendar, or date.

```
GET https://connect.mindcloud.co/v1/universal/datelist/latest/actions/list-booked-slots
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Datelist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/datelist/latest/actions/list-booked-slots?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/datelist/latest/actions/list-booked-slots?${params}`, {
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
| `email` | string | no | Only return booked slots matching a specific email. |
| `calendarId` | number | no | Only return booked slots for a specific calendar. |
| `from` | string | no | Only return booked slots starting from this ISO 8601 date-time. |
| `to` | string | no | Only return booked slots up to this ISO 8601 date-time. |

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

Through the native Datelist API, this operation is `GET /booked_slots` (base URL `https://datelist.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-booked-slots.md) for the provider-specific parameters and requirements.

