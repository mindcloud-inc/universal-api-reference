# Zoho Calendar: Partial Update Event

Updates specific event fields in Zoho Calendar.

```
PUT https://connect.mindcloud.co/v1/universal/zohoCalendar/latest/actions/partial-update-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Calendar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zohoCalendar/latest/actions/partial-update-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "calendarUid": "string",
  "eventUid": "string",
  "eventData": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoCalendar/latest/actions/partial-update-event', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "calendarUid": "string",
    "eventUid": "string",
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
| `eventUid` | string | yes | Event unique identifier. |
| `eventData` | object | yes | Event payload object with the partial fields to update. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "events": [
        {
          "caluid": "string",
          "dateandtime": {
            "end": "string",
            "start": "string",
            "timezone": "string"
          },
          "description": "string",
          "estatus": "string",
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
| `events[].dateandtime.end` | string |  |
| `events[].dateandtime.start` | string |  |
| `events[].dateandtime.timezone` | string |  |
| `events[].description` | string |  |
| `events[].estatus` | string |  |
| `events[].etag` | string |  |
| `events[].isallday` | boolean |  |
| `events[].isApproved` | boolean |  |
| `events[].location` | string |  |
| `events[].organizer` | string |  |
| `events[].title` | string |  |
| `events[].uid` | string |  |
| `events[].viewEventURL` | string |  |

## Native endpoint

Through the native Zoho Calendar API, this operation is `PATCH /calendars/:calendaruid/events/:eventuid` (base URL `https://calendar.zoho.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/partial-update-event.md) for the provider-specific parameters and requirements.

