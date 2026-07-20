# vPlan: Get Attachment



```
GET https://connect.mindcloud.co/v1/universal/vPlan/latest/actions/get-attachment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a vPlan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vPlan/latest/actions/get-attachment?connectionId=$CONNECTION_ID&collectionId=string&attachmentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "collectionId": "string",
  "attachmentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vPlan/latest/actions/get-attachment?${params}`, {
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
| `collectionId` | string | yes |  |
| `attachmentId` | string | yes | Attachment identifier. |

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
| `deleted_at` | string | Deletion timestamp. |
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

Through the native vPlan API, this operation is `GET /collection/[:collection_id]/attachment/[:attachment_id]` (base URL `https://api.vplan.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-attachment.md) for the provider-specific parameters and requirements.

