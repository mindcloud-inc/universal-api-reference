# Open AI: Create Conversation Item

Creates items in a conversation in Open AI.

```
POST https://connect.mindcloud.co/v1/universal/openAi/latest/actions/create-conversation-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Open AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/openAi/latest/actions/create-conversation-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "conversation_id": "string",
  "items[]": [
    {
      "role": "user",
      "type": "message",
      "content": [
        {
          "text": "Hello from MindCloud.",
          "type": "input_text"
        }
      ]
    }
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/openAi/latest/actions/create-conversation-item', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "conversation_id": "string",
    "items[]": [{"role":"user","type":"message","content":[{"text":"Hello from MindCloud.","type":"input_text"}]}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `conversation_id` | string | yes | Conversation ID that will receive the item. |
| `items[]` | array<object> | yes | Items to append to the conversation. Default: `[{"role":"user","type":"message","content":[{"text":"Hello from MindCloud.","type":"input_text"}]}]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
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
      "first_id": "string",
      "has_more": true,
      "last_id": "string",
      "object": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].content[].text` | string | Input text. |
| `data[].content[].type` | string | Content type. |
| `data[].id` | string | Conversation item ID. |
| `data[].role` | string | Role for message items. |
| `data[].status` | string | Item status. |
| `data[].type` | string | Conversation item type. |
| `first_id` | string | First item ID. |
| `has_more` | boolean | Whether more items are available. |
| `last_id` | string | Last item ID. |
| `object` | string | List object type. |

## Native endpoint

Through the native Open AI API, this operation is `POST v1/conversations/:conversation_id/items` (base URL `https://api.openai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-conversation-item.md) for the provider-specific parameters and requirements.

