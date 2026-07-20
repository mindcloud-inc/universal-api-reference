# ChatDaddy: List Chat Messages

Retrieves messages from a chat in ChatDaddy.

```
GET https://connect.mindcloud.co/v1/universal/chatDaddy/latest/actions/list-chat-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChatDaddy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatDaddy/latest/actions/list-chat-messages?connectionId=$CONNECTION_ID&accountId=acc_9d2c3b61-174e-42c5-be_0804&chatId=sample-chat-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "acc_9d2c3b61-174e-42c5-be_0804",
  "chatId": "sample-chat-id"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatDaddy/latest/actions/list-chat-messages?${params}`, {
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
| `accountId` | string | yes | Account identifier for the chat. Default: `acc_9d2c3b61-174e-42c5-be_0804`. |
| `chatId` | string | yes | Chat identifier to fetch messages for. Default: `sample-chat-id`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": "string",
      "chatId": "string",
      "createdAt": "string",
      "id": "string",
      "text": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | string |  |
| `chatId` | string |  |
| `createdAt` | string |  |
| `id` | string |  |
| `text` | string |  |

## Native endpoint

Through the native ChatDaddy API, this operation is `GET /messages/{accountId}/{chatId}` (base URL `https://api.chatdaddy.tech/im`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-chat-messages.md) for the provider-specific parameters and requirements.

