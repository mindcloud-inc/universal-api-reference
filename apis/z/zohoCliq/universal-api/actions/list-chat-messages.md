# Zoho Cliq: List Chat Messages

Retrieves messages from a Zoho Cliq chat.

```
GET https://connect.mindcloud.co/v1/universal/zohoCliq/latest/actions/list-chat-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Cliq `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoCliq/latest/actions/list-chat-messages?connectionId=$CONNECTION_ID&chatId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "chatId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoCliq/latest/actions/list-chat-messages?${params}`, {
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
| `chatId` | string | yes | The ID of the chat whose messages should be retrieved. |
| `fromTime` | number | no | Retrieve messages sent after this time in milliseconds. |
| `toTime` | number | no | Retrieve messages sent before this time in milliseconds. |
| `limit` | number | no | The number of messages to retrieve. Default and maximum is 100. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |

## Native endpoint

Through the native Zoho Cliq API, this operation is `GET /chats/:chatId/messages` (base URL `https://cliq.zoho.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-chat-messages.md) for the provider-specific parameters and requirements.

