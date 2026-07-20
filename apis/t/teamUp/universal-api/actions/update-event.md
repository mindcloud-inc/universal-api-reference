# TeamUp: Update Event

Updates an existing event in TeamUp.

```
PUT https://connect.mindcloud.co/v1/universal/teamUp/latest/actions/update-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TeamUp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/teamUp/latest/actions/update-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "eventId": "string",
  "startDt": "string",
  "endDt": "string",
  "subcalendarIds[]": [
    1
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/teamUp/latest/actions/update-event', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "eventId": "string",
    "startDt": "string",
    "endDt": "string",
    "subcalendarIds[]": [1]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `eventId` | string | yes | The TeamUp event identifier. |
| `startDt` | string | yes | Updated event start datetime in TeamUp format. |
| `endDt` | string | yes | Updated event end datetime in TeamUp format. |
| `subcalendarIds[]` | array<number> | yes | List of TeamUp sub-calendar IDs to assign to the event. |
| `title` | string | no | Updated event title. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "event": {
        "endDt": "string",
        "id": "string",
        "startDt": "string",
        "subcalendarIds": [
          [
            1
          ]
        ],
        "title": "string"
      },
      "undoId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `event` | object |  |
| `event.endDt` | string |  |
| `event.id` | string |  |
| `event.startDt` | string |  |
| `event.subcalendarIds[]` | array<number> |  |
| `event.title` | string |  |
| `undoId` | string |  |

## Native endpoint

Through the native TeamUp API, this operation is `PUT /:calendarKeyOrId/events/:eventId` (base URL `https://api.teamup.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-event.md) for the provider-specific parameters and requirements.

