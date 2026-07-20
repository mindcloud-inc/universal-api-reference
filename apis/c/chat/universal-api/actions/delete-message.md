# 2Chat: Delete Message

Deletes a WhatsApp message from 2Chat.

```
DELETE https://connect.mindcloud.co/v1/universal/chat/latest/actions/delete-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 2Chat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/chat/latest/actions/delete-message?connectionId=$CONNECTION_ID&session_key=string&message_uuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "session_key": "string",
  "message_uuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chat/latest/actions/delete-message?${params}`, {
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
| `session_key` | string | yes | The WhatsApp session key that owns the message. |
| `message_uuid` | string | yes | The UUID of the message to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "messageUuid": "string",
      "success": true,
      "whatsappMessageId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `messageUuid` | string |  |
| `success` | boolean |  |
| `whatsappMessageId` | string |  |

## Native endpoint

Through the native 2Chat API, this operation is `DELETE /whatsapp/message/:session_key/:message_uuid` (base URL `https://api.p.2chat.io/open`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-message.md) for the provider-specific parameters and requirements.

