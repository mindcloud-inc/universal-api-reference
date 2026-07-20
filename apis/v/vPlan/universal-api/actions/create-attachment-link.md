# vPlan: Create Attachment Link



```
POST https://connect.mindcloud.co/v1/universal/vPlan/latest/actions/create-attachment-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a vPlan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/vPlan/latest/actions/create-attachment-link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "collectionId": "41ea0941-d431-4790-b328-f25b36f51326",
  "filename": "codex-link.txt",
  "file": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vPlan/latest/actions/create-attachment-link', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "collectionId": "41ea0941-d431-4790-b328-f25b36f51326",
    "filename": "codex-link.txt",
    "file": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cardId` | string | no | Optional card to attach the link to. |
| `collectionId` | string | yes | Default: `41ea0941-d431-4790-b328-f25b36f51326`. |
| `type` | string | no | Attachment provider/type label. Default: `external`. |
| `filename` | string | yes | Attachment filename. Default: `codex-link.txt`. |
| `file` | string | yes | Public URL for the attachment link. Default: `https://example.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bytes": 1,
      "card_id": "string",
      "checksum": "string",
      "collection_id": "string",
      "created_at": "string",
      "deleted_at": "string",
      "external_ref": "string",
      "file": "string",
      "filename": "Ava Chen",
      "id": "string",
      "signature": "string",
      "thumbnail": "string",
      "thumbnail_bytes": 1,
      "thumbnail_checksum": "string",
      "thumbnail_signature": "string",
      "thumbnail_type": "string",
      "type": "string",
      "updated_at": "string",
      "user_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bytes` | number | Attachment size in bytes. |
| `card_id` | string | Attached card identifier when present. |
| `checksum` | string | File checksum. |
| `collection_id` | string | Collection identifier. |
| `created_at` | string | Creation timestamp. |
| `deleted_at` | string | Deletion timestamp when removed. |
| `external_ref` | string | External reference. |
| `file` | string | Attachment URL. |
| `filename` | string | Attachment filename. |
| `id` | string | Attachment identifier. |
| `signature` | string | File signature. |
| `thumbnail` | string | Thumbnail URL. |
| `thumbnail_bytes` | number | Thumbnail size in bytes. |
| `thumbnail_checksum` | string | Thumbnail checksum. |
| `thumbnail_signature` | string | Thumbnail signature. |
| `thumbnail_type` | string | Thumbnail storage type. |
| `type` | string | Normalized attachment type. |
| `updated_at` | string | Last update timestamp. |
| `user_id` | string | User who created the attachment. |

## Native endpoint

Through the native vPlan API, this operation is `POST /collection/[:collection_id]/attachment` (base URL `https://api.vplan.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-attachment-link.md) for the provider-specific parameters and requirements.

