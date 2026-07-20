# ChatBotKit: List Conversation Messages



```
GET https://connect.mindcloud.co/v1/universal/chatBotKit/latest/actions/list-conversation-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChatBotKit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatBotKit/latest/actions/list-conversation-messages?connectionId=$CONNECTION_ID&conversationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "conversationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatBotKit/latest/actions/list-conversation-messages?${params}`, {
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
| `conversationId` | string | yes | The ID of the conversation to list messages for |
| `cursor` | string | no | The cursor to use for pagination |
| `order` | list | no | The order of the paginated items One of: `asc`, `desc`. |
| `take` | number | no | The number of items to retrieve |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cursor": "string",
      "items": [
        {
          "createdAt": 1,
          "description": "string",
          "id": "string",
          "name": "Ava Chen",
          "text": "string",
          "type": "string",
          "updatedAt": 1
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cursor` | string |  |
| `items[].createdAt` | number |  |
| `items[].description` | string |  |
| `items[].id` | string |  |
| `items[].name` | string |  |
| `items[].text` | string |  |
| `items[].type` | string |  |
| `items[].updatedAt` | number |  |

## Native endpoint

Through the native ChatBotKit API, this operation is `GET /conversation/{conversationId}/message/list` (base URL `https://api.chatbotkit.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-conversation-messages.md) for the provider-specific parameters and requirements.

