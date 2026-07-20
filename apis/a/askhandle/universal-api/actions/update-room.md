# AskHandle: Update Room

Updates an existing AskHandle room by label.

```
PUT https://connect.mindcloud.co/v1/universal/askhandle/latest/actions/update-room
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AskHandle `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/askhandle/latest/actions/update-room" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/askhandle/latest/actions/update-room', {
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
| `label` | string | no | The room label. |
| `name` | string | no | Room name. |
| `rating` | number | no | Room rating. |
| `isBotUse` | boolean | no | Whether the bot is enabled. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "greetingMessage": "string",
      "isBotUse": true,
      "isConfirmedForm": true,
      "isSchedulingOnly": true,
      "label": "string",
      "messages": [
        [
          {}
        ]
      ],
      "name": "Ava Chen",
      "rating": 1,
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | Creation timestamp. |
| `greetingMessage` | string | Greeting message. |
| `isBotUse` | boolean | Whether bot usage is enabled. |
| `isConfirmedForm` | boolean | Whether confirmed-form mode is enabled. |
| `isSchedulingOnly` | boolean | Whether the room is scheduling-only. |
| `label` | string | Room label. |
| `messages[]` | array<object> | Room message list. |
| `name` | string | Room name. |
| `rating` | number | Room rating. |
| `uuid` | string | Room UUID. |

## Native endpoint

Through the native AskHandle API, this operation is `PUT /rooms/:label/` (base URL `https://dashboard.askhandle.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-room.md) for the provider-specific parameters and requirements.

