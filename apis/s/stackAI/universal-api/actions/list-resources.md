# Stack AI: List Resources



```
GET https://connect.mindcloud.co/v1/universal/stackAI/latest/actions/list-resources
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stack AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stackAI/latest/actions/list-resources?connectionId=$CONNECTION_ID&knowledgeBaseId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "knowledgeBaseId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stackAI/latest/actions/list-resources?${params}`, {
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
      "current_cursor": "string",
      "data": [
        {}
      ],
      "next_cursor": "string",
      "prev_cursor": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `current_cursor` | string |  |
| `data` | array<object> |  |
| `next_cursor` | string |  |
| `prev_cursor` | string |  |

## Native endpoint

Through the native Stack AI API, this operation is `GET /v1/knowledge-bases/:knowledge_base_id/resources` (base URL `https://api.stack-ai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-resources.md) for the provider-specific parameters and requirements.

