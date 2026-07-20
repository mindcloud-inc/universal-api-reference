# MyMeet.io: List Bookings



```
GET https://connect.mindcloud.co/v1/universal/myMeetio/latest/actions/list-bookings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MyMeet.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/myMeetio/latest/actions/list-bookings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/myMeetio/latest/actions/list-bookings?${params}`, {
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
      "agenda": "string",
      "cancelationReason": "string",
      "clientLanguage": "string",
      "countryCode": "string",
      "deletedAt": "2026-05-07T12:00:00.000Z",
      "guests": "string",
      "id": 1,
      "meeting": [
        {}
      ],
      "meetingAddress": "string",
      "meetingDate": "2026-05-07T12:00:00.000Z",
      "meetingEndTime": "2026-05-07T12:00:00.000Z",
      "meetingTime": "string",
      "mobileNumber": "string",
      "modeOfCommunication": "string",
      "paymentAmount": "string",
      "paymentMethod": "string",
      "rescheduledAt": "2026-05-07T12:00:00.000Z",
      "serviceDuration": 1,
      "serviceId": 1,
      "serviceTitle": "string",
      "summary": "string",
      "userEmail": "ava@example.com",
      "userId": 1,
      "userName": "Ava Chen",
      "userTimezone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agenda` | string |  |
| `cancelationReason` | string |  |
| `clientLanguage` | string |  |
| `countryCode` | string |  |
| `deletedAt` | date |  |
| `guests` | string |  |
| `id` | number |  |
| `meeting` | array<object> |  |
| `meetingAddress` | string |  |
| `meetingDate` | date |  |
| `meetingEndTime` | date |  |
| `meetingTime` | string |  |
| `mobileNumber` | string |  |
| `modeOfCommunication` | string |  |
| `paymentAmount` | string |  |
| `paymentMethod` | string |  |
| `rescheduledAt` | date |  |
| `serviceDuration` | number |  |
| `serviceId` | number |  |
| `serviceTitle` | string |  |
| `summary` | string |  |
| `userEmail` | string |  |
| `userId` | number |  |
| `userName` | string |  |
| `userTimezone` | string |  |

## Native endpoint

Through the native MyMeet.io API, this operation is `GET /get-bookings` (base URL `https://app.mymeet.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-bookings.md) for the provider-specific parameters and requirements.

