# Open AI: List Conversation Items

Retrieves items from a conversation in Open AI.

```
GET https://connect.mindcloud.co/v1/universal/openAi/latest/actions/list-conversation-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Open AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openAi/latest/actions/list-conversation-items?connectionId=$CONNECTION_ID&conversation_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "conversation_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openAi/latest/actions/list-conversation-items?${params}`, {
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
| `conversation_id` | string | yes | Conversation ID to list items for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "id": "string",
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
| `data[].id` | string | Conversation item ID. |
| `data[].type` | string | Conversation item type. |
| `first_id` | string | First item ID. |
| `has_more` | boolean | Whether more items are available. |
| `last_id` | string | Last item ID. |
| `object` | string | List object type. |

## Native endpoint

Through the native Open AI API, this operation is `GET v1/conversations/:conversation_id/items` (base URL `https://api.openai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-conversation-items.md) for the provider-specific parameters and requirements.

