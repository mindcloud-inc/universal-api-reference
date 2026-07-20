# vPlan: Update Comment



```
PUT https://connect.mindcloud.co/v1/universal/vPlan/latest/actions/update-comment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a vPlan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/vPlan/latest/actions/update-comment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "collectionId": "41ea0941-d431-4790-b328-f25b36f51326",
  "commentId": "ced8aae8-ddbf-4586-8009-4ff4e063a62c"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vPlan/latest/actions/update-comment', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "collectionId": "41ea0941-d431-4790-b328-f25b36f51326",
    "commentId": "ced8aae8-ddbf-4586-8009-4ff4e063a62c"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `collectionId` | string | yes | Default: `41ea0941-d431-4790-b328-f25b36f51326`. |
| `commentId` | string | yes | Comment identifier. Default: `ced8aae8-ddbf-4586-8009-4ff4e063a62c`. |
| `text` | string | no | Updated comment text. Default: `Codex validation comment updated again`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "card_id": "string",
      "collection_id": "string",
      "created_at": "string",
      "deleted_at": "string",
      "id": "string",
      "parent_id": "string",
      "text": "string",
      "updated_at": "string",
      "user_id": "string",
      "user_mentions": [
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
| `card_id` | string | Attached card identifier when present. |
| `collection_id` | string | Collection identifier. |
| `created_at` | string | Creation timestamp. |
| `deleted_at` | string | Deletion timestamp. |
| `id` | string | Comment identifier. |
| `parent_id` | string | Parent comment identifier. |
| `text` | string | Comment text. |
| `updated_at` | string | Last update timestamp. |
| `user_id` | string | Author identifier. |
| `user_mentions` | array<object> | Mentioned users. |

## Native endpoint

Through the native vPlan API, this operation is `PUT /collection/[:collection_id]/comment/[:comment_id]` (base URL `https://api.vplan.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-comment.md) for the provider-specific parameters and requirements.

