# Stack AI: Create Knowledge Base



```
POST https://connect.mindcloud.co/v1/universal/stackAI/latest/actions/create-knowledge-base
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stack AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/stackAI/latest/actions/create-knowledge-base" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/stackAI/latest/actions/create-knowledge-base', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | no | The knowledge base name. |
| `description` | string | no | The knowledge base description. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "connection_source_ids": [
        "string"
      ],
      "created_at": "string",
      "description": "string",
      "is_empty": true,
      "knowledge_base_id": "string",
      "last_synced_at": "string",
      "name": "Ava Chen",
      "total_error_files": 1,
      "total_files": 1,
      "total_indexed_files": 1,
      "total_size": 1,
      "updated_at": "string",
      "website_sources": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `connection_source_ids` | array<string> |  |
| `created_at` | string |  |
| `description` | string |  |
| `is_empty` | boolean |  |
| `knowledge_base_id` | string |  |
| `last_synced_at` | string |  |
| `name` | string |  |
| `total_error_files` | number |  |
| `total_files` | number |  |
| `total_indexed_files` | number |  |
| `total_size` | number |  |
| `updated_at` | string |  |
| `website_sources` | array<string> |  |

## Native endpoint

Through the native Stack AI API, this operation is `POST /v1/knowledge-bases` (base URL `https://api.stack-ai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-knowledge-base.md) for the provider-specific parameters and requirements.

