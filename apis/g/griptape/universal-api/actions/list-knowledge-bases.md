# Griptape: List Knowledge Bases

Finds knowledge bases in Griptape.

```
GET https://connect.mindcloud.co/v1/universal/griptape/latest/actions/list-knowledge-bases
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Griptape `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/griptape/latest/actions/list-knowledge-bases?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/griptape/latest/actions/list-knowledge-bases?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "knowledge_bases": [
        {
          "asset_paths": [
            "string"
          ],
          "bucket_id": "string",
          "created_at": "string",
          "created_by": "string",
          "description": "string",
          "knowledge_base_id": "string",
          "name": "Ava Chen",
          "organization_id": "string",
          "schedule_expression": "string",
          "type": "string",
          "updated_at": "string"
        }
      ],
      "pagination": {
        "page_number": 1,
        "page_size": 1,
        "total_count": 1,
        "total_pages": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `knowledge_bases[].asset_paths` | array<string> |  |
| `knowledge_bases[].bucket_id` | string |  |
| `knowledge_bases[].created_at` | string |  |
| `knowledge_bases[].created_by` | string |  |
| `knowledge_bases[].description` | string |  |
| `knowledge_bases[].knowledge_base_id` | string |  |
| `knowledge_bases[].name` | string |  |
| `knowledge_bases[].organization_id` | string |  |
| `knowledge_bases[].schedule_expression` | string |  |
| `knowledge_bases[].type` | string |  |
| `knowledge_bases[].updated_at` | string |  |
| `pagination.page_number` | number |  |
| `pagination.page_size` | number |  |
| `pagination.total_count` | number |  |
| `pagination.total_pages` | number |  |

## Native endpoint

Through the native Griptape API, this operation is `GET /api/knowledge-bases` (base URL `https://cloud.griptape.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-knowledge-bases.md) for the provider-specific parameters and requirements.

