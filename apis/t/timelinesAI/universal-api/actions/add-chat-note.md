# TimelinesAI: Add Chat Note

Creates a note on an existing TimelinesAI chat.

```
POST https://connect.mindcloud.co/v1/universal/timelinesAI/latest/actions/add-chat-note
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TimelinesAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/timelinesAI/latest/actions/add-chat-note" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "chatId": 1,
  "text": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/timelinesAI/latest/actions/add-chat-note', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "chatId": 1,
    "text": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `chatId` | number | yes | ID of the chat in TimelinesAI. You can find it in the chat URL or outbound webhook payload. |
| `text` | string | yes | Note text to add to the chat. |
| `isPrivate` | boolean | no | Mark the note as private or visible to teammates. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "messageUid": "string"
      },
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `data.messageUid` | string |  |
| `status` | string |  |

## Native endpoint

Through the native TimelinesAI API, this operation is `POST /chats/{chat_id}/notes` (base URL `https://app.timelines.ai/integrations/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-chat-note.md) for the provider-specific parameters and requirements.

