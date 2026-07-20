# Open AI: Delete Conversation Item

Deletes an item from a conversation in Open AI.

```
DELETE https://connect.mindcloud.co/v1/universal/openAi/latest/actions/delete-conversation-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Open AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/openAi/latest/actions/delete-conversation-item?connectionId=$CONNECTION_ID&conversation_id=string&item_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "conversation_id": "string",
  "item_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openAi/latest/actions/delete-conversation-item?${params}`, {
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
| `item_id` | string | yes | Conversation item ID to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": 1,
      "id": "string",
      "metadata": {},
      "object": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | number | Creation timestamp. |
| `id` | string | Conversation ID. |
| `metadata` | object | Conversation metadata. |
| `object` | string | Object type. |

## Native endpoint

Through the native Open AI API, this operation is `DELETE v1/conversations/:conversation_id/items/:item_id` (base URL `https://api.openai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-conversation-item.md) for the provider-specific parameters and requirements.

