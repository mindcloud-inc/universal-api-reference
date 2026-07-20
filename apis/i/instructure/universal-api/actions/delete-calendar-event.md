# Instructure: Delete Calendar Event

Deletes a calendar event from Instructure Canvas.

```
DELETE https://connect.mindcloud.co/v1/universal/instructure/latest/actions/delete-calendar-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instructure `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/instructure/latest/actions/delete-calendar-event?connectionId=$CONNECTION_ID&eventId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "eventId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instructure/latest/actions/delete-calendar-event?${params}`, {
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
| `eventId` | string | yes | The Canvas calendar event ID. Default: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allDay": true,
      "contextCode": "string",
      "description": "string",
      "endAt": "string",
      "htmlUrl": "https://example.com",
      "id": 1,
      "locationName": "Ava Chen",
      "startAt": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allDay` | boolean |  |
| `contextCode` | string |  |
| `description` | string |  |
| `endAt` | string |  |
| `htmlUrl` | string |  |
| `id` | number |  |
| `locationName` | string |  |
| `startAt` | string |  |
| `title` | string |  |

## Native endpoint

Through the native Instructure API, this operation is `DELETE /calendar_events/:event_id` (base URL `https://canvas.instructure.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-calendar-event.md) for the provider-specific parameters and requirements.

