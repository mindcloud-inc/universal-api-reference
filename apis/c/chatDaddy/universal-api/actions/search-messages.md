# ChatDaddy: Search Messages

Finds message records in your ChatDaddy account.

```
GET https://connect.mindcloud.co/v1/universal/chatDaddy/latest/actions/search-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChatDaddy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatDaddy/latest/actions/search-messages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatDaddy/latest/actions/search-messages?${params}`, {
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
| `q` | string | no | Search messages by text. |

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
| `accountId` | string | Account identifier. |
| `chatId` | string | Chat identifier. |
| `createdAt` | string | ISO timestamp when the message was created. |
| `id` | string | Message identifier. |
| `text` | string | Message text content. |

## Native endpoint

Through the native ChatDaddy API, this operation is `GET /messages/search` (base URL `https://api.chatdaddy.tech/im`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-messages.md) for the provider-specific parameters and requirements.

