# vPlan: Update Collection



```
PUT https://connect.mindcloud.co/v1/universal/vPlan/latest/actions/update-collection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a vPlan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/vPlan/latest/actions/update-collection" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "6ed85855-b5b4-41df-9134-1c9e518f52c5",
  "name": "Codex Action Collection Updated"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vPlan/latest/actions/update-collection', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "6ed85855-b5b4-41df-9134-1c9e518f52c5",
    "name": "Codex Action Collection Updated"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Collection identifier. Default: `6ed85855-b5b4-41df-9134-1c9e518f52c5`. |
| `name` | string | yes | Collection name. Default: `Codex Action Collection Updated`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "batch_id": "string",
      "board_id": "string",
      "cover_color_hex": "string",
      "cover_image_bytes": 1,
      "cover_image_checksum": "string",
      "cover_image_signature": "string",
      "cover_image_url": "https://example.com",
      "created_at": "string",
      "custom_fields": [
        {}
      ],
      "deleted_at": "string",
      "description": "string",
      "due_date": "string",
      "end": "string",
      "external_ref": "string",
      "id": "string",
      "meta": {},
      "name": "Ava Chen",
      "position": 1,
      "progress": "string",
      "source_type": "string",
      "start": "string",
      "status": "string",
      "updated_at": "string",
      "warnings": [
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
| `batch_id` | string | Batch identifier when present. |
| `board_id` | string | Parent board identifier. |
| `cover_color_hex` | string | Cover color. |
| `cover_image_bytes` | number | Cover image size in bytes. |
| `cover_image_checksum` | string | Cover image checksum. |
| `cover_image_signature` | string | Cover image signature. |
| `cover_image_url` | string | Cover image URL. |
| `created_at` | string | Creation timestamp. |
| `custom_fields` | array<object> | Custom field values. |
| `deleted_at` | string | Deletion timestamp. |
| `description` | string | Collection description. |
| `due_date` | string | Due date. |
| `end` | string | End date. |
| `external_ref` | string | External reference. |
| `id` | string | Collection identifier. |
| `meta` | object | Additional metadata. |
| `name` | string | Collection name. |
| `position` | number | Collection position. |
| `progress` | string | Collection progress. |
| `source_type` | string | Collection source type. |
| `start` | string | Start date. |
| `status` | string | Collection status. |
| `updated_at` | string | Last update timestamp. |
| `warnings` | array<object> | Collection warnings. |

## Native endpoint

Through the native vPlan API, this operation is `PUT /collection/[:id]` (base URL `https://api.vplan.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-collection.md) for the provider-specific parameters and requirements.

