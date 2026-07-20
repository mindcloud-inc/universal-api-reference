# Samedi: Guest Book Appointment

Books an appointment in Samedi for a guest.

```
POST https://connect.mindcloud.co/v1/universal/samedi/latest/actions/guest-book-appointment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Samedi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/samedi/latest/actions/guest-book-appointment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "eventCategoryId": "string",
  "eventTypeId": "string",
  "startsAt": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/samedi/latest/actions/guest-book-appointment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "eventCategoryId": "string",
    "eventTypeId": "string",
    "startsAt": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `eventCategoryId` | string | yes | Appointment category ID for the booking. |
| `eventTypeId` | string | yes | Appointment type ID for the booking. |
| `startsAt` | string | yes | Selected appointment start timestamp. |
| `attendant.data.firstName` | string | no | Patient first name for booking without a samedi patient user. |
| `attendant.data.lastName` | string | no | Patient last name for booking without a samedi patient user. |
| `attendant.data.email` | string | no | Patient email for booking without a samedi patient user. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Samedi API returns.

## Native endpoint

Through the native Samedi API, this operation is `POST /booking/v3/book` (base URL `https://patient.samedi.de/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/guest-book-appointment.md) for the provider-specific parameters and requirements.

