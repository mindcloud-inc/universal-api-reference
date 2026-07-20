# Instructure: List Calendar Events

Retrieves calendar events from Instructure Canvas.

```
GET https://connect.mindcloud.co/v1/universal/instructure/latest/actions/list-calendar-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instructure `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instructure/latest/actions/list-calendar-events?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instructure/latest/actions/list-calendar-events?${params}`, {
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

Through the native Instructure API, this operation is `GET /calendar_events` (base URL `https://canvas.instructure.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-calendar-events.md) for the provider-specific parameters and requirements.

