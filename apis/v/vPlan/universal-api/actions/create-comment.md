# vPlan: Create Comment



```
POST https://connect.mindcloud.co/v1/universal/vPlan/latest/actions/create-comment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a vPlan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/vPlan/latest/actions/create-comment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "collectionId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vPlan/latest/actions/create-comment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "collectionId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `collectionId` | string | yes |  |
| `text` | string | no | Comment text. |

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

Through the native vPlan API, this operation is `POST /collection/[:collection_id]/comment` (base URL `https://api.vplan.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-comment.md) for the provider-specific parameters and requirements.

