# Zoho Calendar: Get Group Attendees Details

Retrieves group attendee details for an event in Zoho Calendar.

```
GET https://connect.mindcloud.co/v1/universal/zohoCalendar/latest/actions/get-group-attendees-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Calendar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoCalendar/latest/actions/get-group-attendees-details?connectionId=$CONNECTION_ID&calendarUid=string&eventUid=string&groupId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "calendarUid": "string",
  "eventUid": "string",
  "groupId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoCalendar/latest/actions/get-group-attendees-details?${params}`, {
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
| `calendarUid` | string | yes | Calendar unique identifier. |
| `eventUid` | string | yes | Event unique identifier. |
| `groupId` | number | yes | Numeric group identifier for the attendee status lookup. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Zoho Calendar API returns.

## Native endpoint

Through the native Zoho Calendar API, this operation is `GET /calendars/:calendaruid/events/:eventuid/groupattendeestatus` (base URL `https://calendar.zoho.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-group-attendees-details.md) for the provider-specific parameters and requirements.

