# Zoho Calendar: Get Event Details

Retrieves details for an event in Zoho Calendar.

```
GET https://connect.mindcloud.co/v1/universal/zohoCalendar/latest/actions/get-event-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Calendar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoCalendar/latest/actions/get-event-details?connectionId=$CONNECTION_ID&calendarUid=string&eventUid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "calendarUid": "string",
  "eventUid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoCalendar/latest/actions/get-event-details?${params}`, {
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
| `calendarUid` | string | yes | Calendar unique identifier for the event. |
| `eventUid` | string | yes | Event unique identifier. |
| `recurrenceId` | string | no | Specific recurrence instance identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "events": [
        {
          "caluid": "string",
          "createdby": "string",
          "dateandtime": {
            "end": "string",
            "start": "string",
            "timezone": "string"
          },
          "description": "string",
          "etag": "string",
          "isallday": true,
          "isApproved": true,
          "location": "string",
          "organizer": "string",
          "title": "string",
          "uid": "string",
          "viewEventURL": "https://example.com"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `events[].caluid` | string |  |
| `events[].createdby` | string |  |
| `events[].dateandtime.end` | string |  |
| `events[].dateandtime.start` | string |  |
| `events[].dateandtime.timezone` | string |  |
| `events[].description` | string |  |
| `events[].etag` | string |  |
| `events[].isallday` | boolean |  |
| `events[].isApproved` | boolean |  |
| `events[].location` | string |  |
| `events[].organizer` | string |  |
| `events[].title` | string |  |
| `events[].uid` | string |  |
| `events[].viewEventURL` | string |  |

## Native endpoint

Through the native Zoho Calendar API, this operation is `GET /calendars/:calendaruid/events/:eventuid` (base URL `https://calendar.zoho.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-event-details.md) for the provider-specific parameters and requirements.

