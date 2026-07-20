# 2Chat: Get a Message

Retrieves a WhatsApp message from 2Chat.

```
GET https://connect.mindcloud.co/v1/universal/chat/latest/actions/get-a-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 2Chat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chat/latest/actions/get-a-message?connectionId=$CONNECTION_ID&session_key=string&message_uuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "session_key": "string",
  "message_uuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chat/latest/actions/get-a-message?${params}`, {
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
| `message_uuid` | string | yes | The UUID of the message to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": {
        "createdAt": "2026-05-07T12:00:00.000Z",
        "id": "string",
        "isFromAgent": true,
        "isFromApi": true,
        "isFromChatter": true,
        "isFromFlowRun": true,
        "message": {
          "text": "string"
        },
        "processed": true,
        "sentBy": "string",
        "sessionKey": "string",
        "uuid": "string",
        "waMsgAck": {},
        "waMsgId": {}
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message.createdAt` | date |  |
| `message.id` | string |  |
| `message.isFromAgent` | boolean |  |
| `message.isFromApi` | boolean |  |
| `message.isFromChatter` | boolean |  |
| `message.isFromFlowRun` | boolean |  |
| `message.message.text` | string |  |
| `message.processed` | boolean |  |
| `message.sentBy` | string |  |
| `message.sessionKey` | string |  |
| `message.uuid` | string |  |
| `message.waMsgAck` | object |  |
| `message.waMsgId` | object |  |
| `success` | boolean |  |

## Native endpoint

Through the native 2Chat API, this operation is `GET /whatsapp/message/:session_key/:message_uuid` (base URL `https://api.p.2chat.io/open`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-a-message.md) for the provider-specific parameters and requirements.

