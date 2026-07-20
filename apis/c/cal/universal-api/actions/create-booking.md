# Cal.com: Create Booking

Creates a booking in Cal.com.

```
POST https://connect.mindcloud.co/v1/universal/cal/latest/actions/create-booking
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cal.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cal/latest/actions/create-booking" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "start": "string",
  "attendee": {},
  "attendee.name": "Ava Chen",
  "attendee.timeZone": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cal/latest/actions/create-booking', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "start": "string",
    "attendee": {},
    "attendee.name": "Ava Chen",
    "attendee.timeZone": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `start` | string | yes | Booking start time in ISO 8601 UTC format. |
| `attendee` | object | yes | Attendee object including at least name and timeZone. |
| `attendee.name` | string | yes | Attendee full name. |
| `attendee.email` | string | no | Attendee email address. |
| `attendee.timeZone` | string | yes | Attendee IANA time zone. |
| `attendee.language` | string | no | Attendee language code. |
| `attendee.phoneNumber` | string | no | Attendee phone number. |
| `eventTypeId` | list | no | Event type ID to book when using ID-based routing. |
| `eventTypeSlug` | list | no | Event type slug to book when using slug-based routing. |
| `username` | string | no | Username owner for the event type route. |
| `teamSlug` | string | no | Team slug for team-scoped booking routes. |
| `organizationSlug` | string | no | Organization slug for org-scoped booking routes. |
| `guests[]` | array<string> | no | Guest email list to include in the booking. |
| `meetingUrl` | string | no | Override meeting URL for this booking. |
| `location` | object | no | Booking location payload. |
| `location.type` | string | no | Location type discriminator. |
| `location.location` | string | no | Location value for custom location types. |
| `location.address` | string | no | Address value when using physical/in-person location types. |
| `location.phone` | string | no | Phone number when using phone location types. |
| `location.integration` | string | no | Integration identifier for integration-backed location types. |
| `bookingFieldsResponses` | object | no | Dynamic booking field responses map. |
| `metadata` | object | no | Custom metadata object for the booking. |
| `lengthInMinutes` | number | no | Override booking duration in minutes. |
| `routing` | object | no | Routing payload for round-robin or queued routing. |
| `routing.queuedResponseId` | string | no | Queued routing response identifier. |
| `routing.responseId` | number | no | Routing response identifier. |
| `routing.teamMemberIds[]` | array<number> | no | Candidate team member IDs for routing. |
| `routing.teamMemberEmail` | string | no | Team member email for routing. |
| `routing.skipContactOwner` | boolean | no | Skip assigning the contact owner during routing. |
| `routing.crmAppSlug` | string | no | CRM app slug used by routing rules. |
| `routing.crmOwnerRecordType` | string | no | CRM owner record type used in routing. |
| `emailVerificationCode` | string | no | Email verification code for protected event types. |
| `instant` | boolean | no | Create instant booking when supported. |
| `recurrenceCount` | number | no | Recurring booking count for recurring event types. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attendees": [
        {}
      ],
      "createdAt": "string",
      "description": "string",
      "duration": 1,
      "end": "string",
      "eventTypeId": 1,
      "guests": [
        "string"
      ],
      "id": 1,
      "location": "string",
      "meetingUrl": "https://example.com",
      "metadata": {},
      "start": "string",
      "status": "string",
      "title": "string",
      "uid": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attendees` | array<object> |  |
| `createdAt` | string |  |
| `description` | string |  |
| `duration` | number |  |
| `end` | string |  |
| `eventTypeId` | number |  |
| `guests` | array<string> |  |
| `id` | number |  |
| `location` | string |  |
| `meetingUrl` | string |  |
| `metadata` | object |  |
| `start` | string |  |
| `status` | string |  |
| `title` | string |  |
| `uid` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Cal.com API, this operation is `POST /bookings` (base URL `https://api.cal.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-booking.md) for the provider-specific parameters and requirements.

