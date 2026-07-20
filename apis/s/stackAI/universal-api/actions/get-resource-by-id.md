# Stack AI: Get Resource by ID



```
GET https://connect.mindcloud.co/v1/universal/stackAI/latest/actions/get-resource-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stack AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stackAI/latest/actions/get-resource-by-id?connectionId=$CONNECTION_ID&knowledgeBaseId=string&resourceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "knowledgeBaseId": "string",
  "resourceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stackAI/latest/actions/get-resource-by-id?${params}`, {
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
| `resourceId` | string | yes | The resource identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content_hash": "string",
      "content_mime": "string",
      "created_at": "string",
      "dataloader_metadata": {},
      "indexed_at": "string",
      "knowledge_base_id": "string",
      "modified_at": "string",
      "resource_id": "string",
      "resource_path": "string",
      "size": 1,
      "status": "string",
      "user_metadata": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content_hash` | string | Content hash for the resource body. |
| `content_mime` | string | Detected MIME type for the resource. |
| `created_at` | string | When the resource was created. |
| `dataloader_metadata` | object | Loader metadata attached to the resource. |
| `indexed_at` | string | When Stack AI indexed the resource, when present. |
| `knowledge_base_id` | string | The knowledge base identifier for the resource. |
| `modified_at` | string | When the resource was last modified. |
| `resource_id` | string | The resource identifier. |
| `resource_path` | string | The resource path or filename. |
| `size` | number | Resource size in bytes. |
| `status` | string | Current Stack AI resource processing status. |
| `user_metadata` | object | User metadata attached to the resource. |

## Native endpoint

Through the native Stack AI API, this operation is `GET /v1/knowledge-bases/:knowledge_base_id/resources/:resource_id` (base URL `https://api.stack-ai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-resource-by-id.md) for the provider-specific parameters and requirements.

