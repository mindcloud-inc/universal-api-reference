# Digital Samba: Create a question in the room

Creates a room question in Digital Samba.

```
POST https://connect.mindcloud.co/v1/universal/digitalSamba/latest/actions/create-a-question-in-the-room
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Digital Samba `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/digitalSamba/latest/actions/create-a-question-in-the-room" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "room": "string",
  "participant": {},
  "question": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/digitalSamba/latest/actions/create-a-question-in-the-room', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "room": "string",
    "participant": {},
    "question": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `room` | string | yes | Room path parameter. |
| `participant` | object | yes | Participant: either { "name", "external_id" } or { "id" } (uuid of existing participant). |
| `question` | string | yes | The question text. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `body` | object | no | JSON request body documented for this endpoint. |
| `anonymous` | boolean | no | Whether to show as anonymous. |
| `breakoutId` | string | no | Must be a valid UUID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Digital Samba API returns.

## Native endpoint

Through the native Digital Samba API, this operation is `POST /rooms/:room/questions` (base URL `https://api.digitalsamba.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-a-question-in-the-room.md) for the provider-specific parameters and requirements.

