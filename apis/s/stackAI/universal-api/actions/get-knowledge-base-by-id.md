# Stack AI: Get Knowledge Base by ID



```
GET https://connect.mindcloud.co/v1/universal/stackAI/latest/actions/get-knowledge-base-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stack AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stackAI/latest/actions/get-knowledge-base-by-id?connectionId=$CONNECTION_ID&knowledgeBaseId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "knowledgeBaseId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stackAI/latest/actions/get-knowledge-base-by-id?${params}`, {
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
| `knowledgeBaseId` | string | yes | The knowledge base identifier. |

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

Through the native Stack AI API, this operation is `GET /v1/knowledge-bases/:knowledge_base_id` (base URL `https://api.stack-ai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-knowledge-base-by-id.md) for the provider-specific parameters and requirements.

