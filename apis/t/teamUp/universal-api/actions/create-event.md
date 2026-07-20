# TeamUp: Create Event

Creates a new event in TeamUp.

```
POST https://connect.mindcloud.co/v1/universal/teamUp/latest/actions/create-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TeamUp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/teamUp/latest/actions/create-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "subcalendarIds[]": [
    1
  ],
  "startDt": "string",
  "endDt": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/teamUp/latest/actions/create-event', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "subcalendarIds[]": [1],
    "startDt": "string",
    "endDt": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `subcalendarIds[]` | array<number> | yes | List of TeamUp sub-calendar IDs to assign to the event. |
| `startDt` | string | yes | Event start datetime in TeamUp format. |
| `endDt` | string | yes | Event end datetime in TeamUp format. |
| `title` | string | no | Event title. |

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

Through the native TeamUp API, this operation is `POST /:calendarKeyOrId/events` (base URL `https://api.teamup.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-event.md) for the provider-specific parameters and requirements.

