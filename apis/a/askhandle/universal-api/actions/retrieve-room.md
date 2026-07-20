# AskHandle: Retrieve Room

Retrieves one AskHandle room by label.

```
GET https://connect.mindcloud.co/v1/universal/askhandle/latest/actions/retrieve-room
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AskHandle `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/askhandle/latest/actions/retrieve-room?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/askhandle/latest/actions/retrieve-room?${params}`, {
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
| `label` | string | no | The room label. |

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

Through the native AskHandle API, this operation is `GET /rooms/:label/` (base URL `https://dashboard.askhandle.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-room.md) for the provider-specific parameters and requirements.

