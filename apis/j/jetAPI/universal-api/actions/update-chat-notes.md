# JetAPI: Update Chat Notes

Updates existing chat notes in JetAPI.

```
PUT https://connect.mindcloud.co/v1/universal/jetAPI/latest/actions/update-chat-notes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a JetAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/jetAPI/latest/actions/update-chat-notes" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "phone": "string",
  "notes[].title": "string",
  "notes[].body": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/jetAPI/latest/actions/update-chat-notes', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "phone": "string",
    "notes[].title": "string",
    "notes[].body": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `phone` | string | yes | Phone number to identify the conversation. |
| `notes[].title` | string | yes | Chat note title. |
| `notes[].body` | string | yes | Chat note content. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tdlibUsername` | string | no | Optional Telegram username identifier. |
| `tdlibUserId` | number | no | Optional Telegram user ID identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "conversations": [
        {}
      ],
      "meta": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `conversations` | array<object> | Conversations updated by the note write operation. |
| `meta` | object | Response metadata. |

## Native endpoint

Through the native JetAPI API, this operation is `PUT /api/developer_chat/conversations/notes` (base URL `https://api.jetapi.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-chat-notes.md) for the provider-specific parameters and requirements.

