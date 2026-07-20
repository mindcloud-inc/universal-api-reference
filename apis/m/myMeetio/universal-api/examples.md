# MyMeet.io Universal API Examples

These examples use the MindCloud API key and MyMeet.io connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Bookings



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

Example response:

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

See the full [List Bookings action reference](actions/list-bookings.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/myMeetio/latest/actions/list-bookings).
