# OnceHub: List Bookings



```
GET https://connect.mindcloud.co/v1/universal/onceHub/latest/actions/list-bookings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OnceHub `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/onceHub/latest/actions/list-bookings?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/onceHub/latest/actions/list-bookings?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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
      "externalCalendar": {},
      "formSubmission": {},
      "icsUrl": "https://example.com",
      "id": "string",
      "inTrash": true,
      "lastUpdatedTime": "2026-05-07T12:00:00.000Z",
      "locationDescription": {},
      "masterPage": {},
      "object": "string",
      "owner": "string",
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
| `externalCalendar` | object |  |
| `formSubmission` | object |  |
| `icsUrl` | string |  |
| `id` | string |  |
| `inTrash` | boolean |  |
| `lastUpdatedTime` | date |  |
| `locationDescription` | object |  |
| `masterPage` | object |  |
| `object` | string |  |
| `owner` | string |  |
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

Through the native OnceHub API, this operation is `GET /v2/bookings` (base URL `https://api.oncehub.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-bookings.md) for the provider-specific parameters and requirements.

