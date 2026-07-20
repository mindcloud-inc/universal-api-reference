# CalendarLink: Get Event

Retrieves an event from a CalendarLink organization.

```
GET https://connect.mindcloud.co/v1/universal/calendarLink/latest/actions/get-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CalendarLink `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/calendarLink/latest/actions/get-event?connectionId=$CONNECTION_ID&event=string&organization=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "event": "string",
  "organization": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/calendarLink/latest/actions/get-event?${params}`, {
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
| `event` | string | yes | CalendarLink event ID. |
| `organization` | string | yes | CalendarLink organization ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "end": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "isRecurring": true,
      "location": "string",
      "locationUrl": "https://example.com",
      "rsvp": {},
      "start": "2026-05-07T12:00:00.000Z",
      "state": "string",
      "timezone": "string",
      "title": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `end` | date |  |
| `id` | string |  |
| `isRecurring` | boolean |  |
| `location` | string |  |
| `locationUrl` | string |  |
| `rsvp` | object |  |
| `start` | date |  |
| `state` | string |  |
| `timezone` | string |  |
| `title` | string |  |
| `url` | string |  |

## Native endpoint

Through the native CalendarLink API, this operation is `GET /:organisation/event/:event` (base URL `https://my.calendarlink.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-event.md) for the provider-specific parameters and requirements.

