# vPlan: Get Comment



```
GET https://connect.mindcloud.co/v1/universal/vPlan/latest/actions/get-comment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a vPlan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vPlan/latest/actions/get-comment?connectionId=$CONNECTION_ID&collectionId=41ea0941-d431-4790-b328-f25b36f51326&commentId=ced8aae8-ddbf-4586-8009-4ff4e063a62c" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "collectionId": "41ea0941-d431-4790-b328-f25b36f51326",
  "commentId": "ced8aae8-ddbf-4586-8009-4ff4e063a62c"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vPlan/latest/actions/get-comment?${params}`, {
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
| `collectionId` | string | yes | Default: `41ea0941-d431-4790-b328-f25b36f51326`. |
| `commentId` | string | yes | Default: `ced8aae8-ddbf-4586-8009-4ff4e063a62c`. |

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
      "user": {},
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
| `user` | object | Expanded user payload. |
| `user_id` | string | Author identifier. |
| `user_mentions` | array<object> | Mentioned users. |

## Native endpoint

Through the native vPlan API, this operation is `GET /collection/[:collection_id]/comment/[:comment_id]` (base URL `https://api.vplan.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-comment.md) for the provider-specific parameters and requirements.

