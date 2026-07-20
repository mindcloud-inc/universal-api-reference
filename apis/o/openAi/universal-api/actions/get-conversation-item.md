# Open AI: Get Conversation Item

Retrieves an item from a conversation in Open AI.

```
GET https://connect.mindcloud.co/v1/universal/openAi/latest/actions/get-conversation-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Open AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openAi/latest/actions/get-conversation-item?connectionId=$CONNECTION_ID&conversation_id=string&item_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "conversation_id": "string",
  "item_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openAi/latest/actions/get-conversation-item?${params}`, {
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
| `conversation_id` | string | yes | Conversation ID that owns the item. |
| `item_id` | string | yes | Conversation item ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": [
        {
          "text": "string",
          "type": "string"
        }
      ],
      "id": "string",
      "role": "string",
      "status": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content[].text` | string | Input text. |
| `content[].type` | string | Content type. |
| `id` | string | Conversation item ID. |
| `role` | string | Role for message items. |
| `status` | string | Item status. |
| `type` | string | Conversation item type. |

## Native endpoint

Through the native Open AI API, this operation is `GET v1/conversations/:conversation_id/items/:item_id` (base URL `https://api.openai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-conversation-item.md) for the provider-specific parameters and requirements.

