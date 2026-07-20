# Griptape: Query Knowledge Base

Queries a knowledge base in Griptape.

```
GET https://connect.mindcloud.co/v1/universal/griptape/latest/actions/query-knowledge-base
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Griptape `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/griptape/latest/actions/query-knowledge-base?connectionId=$CONNECTION_ID&knowledgeBaseId=string&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "knowledgeBaseId": "string",
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/griptape/latest/actions/query-knowledge-base?${params}`, {
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
| `knowledgeBaseId` | string | yes | The knowledge base ID to query. |
| `query` | string | yes | The search query to run against the knowledge base. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "string",
      "created_by": "string",
      "entries": [
        {
          "id": "string",
          "meta": {},
          "namespace": "Ava Chen",
          "score": 1,
          "type": "string",
          "vector": [
            1
          ]
        }
      ],
      "knowledge_base_id": "string",
      "knowledge_base_query_id": "string",
      "query": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string |  |
| `created_by` | string |  |
| `entries[].id` | string |  |
| `entries[].meta` | object |  |
| `entries[].namespace` | string |  |
| `entries[].score` | number |  |
| `entries[].type` | string |  |
| `entries[].vector` | array<number> |  |
| `knowledge_base_id` | string |  |
| `knowledge_base_query_id` | string |  |
| `query` | string |  |

## Native endpoint

Through the native Griptape API, this operation is `POST /api/knowledge-bases/:knowledge_base_id/query` (base URL `https://cloud.griptape.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/query-knowledge-base.md) for the provider-specific parameters and requirements.

