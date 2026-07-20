# Google Calendar: Move Event

Moves an event to another calendar in Google Calendar.

```
PUT https://connect.mindcloud.co/v1/universal/googleCalendar/latest/actions/move-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Calendar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/googleCalendar/latest/actions/move-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleCalendar/latest/actions/move-event', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `calendar` | list | no |  |
| `eventId` | string | no |  |
| `destination` | list | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Google Calendar API returns.

## Native endpoint

Through the native Google Calendar API, this operation is `POST calendars/:calendar/events/:eventId/move` (base URL `https://www.googleapis.com/calendar/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/move-event.md) for the provider-specific parameters and requirements.

