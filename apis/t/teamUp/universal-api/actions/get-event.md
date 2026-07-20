# TeamUp: Get Event

Retrieves a single event from TeamUp.

```
GET https://connect.mindcloud.co/v1/universal/teamUp/latest/actions/get-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TeamUp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/teamUp/latest/actions/get-event?connectionId=$CONNECTION_ID&eventId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "eventId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/teamUp/latest/actions/get-event?${params}`, {
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
| `eventId` | string | yes | The TeamUp event identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "event": {
        "allDay": true,
        "endDt": "string",
        "history": {},
        "id": "string",
        "startDt": "string",
        "subcalendarIds": [
          [
            1
          ]
        ],
        "title": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `event` | object |  |
| `event.allDay` | boolean |  |
| `event.endDt` | string |  |
| `event.history` | object |  |
| `event.id` | string |  |
| `event.startDt` | string |  |
| `event.subcalendarIds[]` | array<number> |  |
| `event.title` | string |  |

## Native endpoint

Through the native TeamUp API, this operation is `GET /:calendarKeyOrId/events/:eventId` (base URL `https://api.teamup.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-event.md) for the provider-specific parameters and requirements.

