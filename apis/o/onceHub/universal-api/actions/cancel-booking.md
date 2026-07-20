# OnceHub: Cancel Booking



```
PUT https://connect.mindcloud.co/v1/universal/onceHub/latest/actions/cancel-booking
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OnceHub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/onceHub/latest/actions/cancel-booking" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/onceHub/latest/actions/cancel-booking', {
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
| `cancellationReason` | string | no | Reason to include with the booking cancellation. Example: `Customer asked to cancel`. |
| `sendCancellationEmail` | boolean | no | Whether OnceHub should email the customer about the cancellation. Example: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attendees": [
        "string"
      ],
      "bookingCalendar": "string",
      "bookingPage": {},
      "cancelRescheduleInformation": {
        "actionedBy": "string",
        "reason": "string",
        "userId": "string"
      },
      "cancelUrl": "https://example.com",
      "contact": "string",
      "conversation": "string",
      "creationTime": "2026-05-07T12:00:00.000Z",
      "customerTimezone": "string",
      "durationMinutes": 1,
      "eventType": {},
      "externalCalendar": {
        "eventId": {},
        "id": {},
        "name": {},
        "type": "string"
      },
      "formSubmission": {},
      "icsUrl": "https://example.com",
      "id": "string",
      "inTrash": true,
      "lastUpdatedTime": "2026-05-07T12:00:00.000Z",
      "locationDescription": {},
      "masterPage": {},
      "object": "string",
      "owner": {
        "email": "ava@example.com",
        "firstName": "Ava",
        "id": "string",
        "lastName": "Chen",
        "object": "string",
        "roleName": "Ava Chen",
        "status": "string",
        "teams": [
          "string"
        ],
        "timezone": "string"
      },
      "paymentInformation": {},
      "rescheduledBookingId": {},
      "rescheduleUrl": "https://example.com",
      "startingTime": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "subject": "string",
      "trackingId": "string",
      "utmParams": {},
      "virtualConferencing": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attendees[]` | string |  |
| `bookingCalendar` | string |  |
| `bookingPage` | object |  |
| `cancelRescheduleInformation.actionedBy` | string |  |
| `cancelRescheduleInformation.reason` | string |  |
| `cancelRescheduleInformation.userId` | string |  |
| `cancelUrl` | string |  |
| `contact` | string |  |
| `conversation` | string |  |
| `creationTime` | date |  |
| `customerTimezone` | string |  |
| `durationMinutes` | number |  |
| `eventType` | object |  |
| `externalCalendar.eventId` | object |  |
| `externalCalendar.id` | object |  |
| `externalCalendar.name` | object |  |
| `externalCalendar.type` | string |  |
| `formSubmission` | object |  |
| `icsUrl` | string |  |
| `id` | string |  |
| `inTrash` | boolean |  |
| `lastUpdatedTime` | date |  |
| `locationDescription` | object |  |
| `masterPage` | object |  |
| `object` | string |  |
| `owner.email` | string |  |
| `owner.firstName` | string |  |
| `owner.id` | string |  |
| `owner.lastName` | string |  |
| `owner.object` | string |  |
| `owner.roleName` | string |  |
| `owner.status` | string |  |
| `owner.teams[]` | string |  |
| `owner.timezone` | string |  |
| `paymentInformation` | object |  |
| `rescheduledBookingId` | object |  |
| `rescheduleUrl` | string |  |
| `startingTime` | date |  |
| `status` | string |  |
| `subject` | string |  |
| `trackingId` | string |  |
| `utmParams` | object |  |
| `virtualConferencing` | object |  |

## Native endpoint

Through the native OnceHub API, this operation is `POST /v2/bookings/:id/cancel` (base URL `https://api.oncehub.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-booking.md) for the provider-specific parameters and requirements.

