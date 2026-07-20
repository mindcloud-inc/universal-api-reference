# Zoho Calendar: Create Event

Creates a new event in Zoho Calendar.

```
POST https://connect.mindcloud.co/v1/universal/zohoCalendar/latest/actions/create-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Calendar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoCalendar/latest/actions/create-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "calendarUid": "string",
  "eventData": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoCalendar/latest/actions/create-event', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "calendarUid": "string",
    "eventData": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `calendarUid` | string | yes | Calendar unique identifier. |
| `eventData` | object | yes | Event payload object describing the new event. |

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
          "rrule": "string",
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
| `events[].rrule` | string |  |
| `events[].title` | string |  |
| `events[].uid` | string |  |
| `events[].viewEventURL` | string |  |

## Native endpoint

Through the native Zoho Calendar API, this operation is `POST /calendars/:calendaruid/events` (base URL `https://calendar.zoho.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-event.md) for the provider-specific parameters and requirements.

