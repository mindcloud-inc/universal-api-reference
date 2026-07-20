# QWIC: Add Knowledge Base Text or File Data Sources

Adds text or file data sources to a QWIC knowledge base.

```
POST https://connect.mindcloud.co/v1/universal/qWIC/latest/actions/add-knowledge-base-text-or-file-data-sources
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QWIC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/qWIC/latest/actions/add-knowledge-base-text-or-file-data-sources" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "knowledgeBaseId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/qWIC/latest/actions/add-knowledge-base-text-or-file-data-sources', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "knowledgeBaseId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `knowledgeBaseId` | number | yes | Knowledge base ID. |
| `textDataSource` | string | no | Plain text content to upload as a knowledge base source. |
| `fileDataSource` | file | no | File content to upload as a knowledge base source. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string |  |

## Native endpoint

Through the native QWIC API, this operation is `POST /api/v1/ai/knowledge-base/:knowledge_base_id/upload/sources` (base URL `https://app.qwic.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-knowledge-base-text-or-file-data-sources.md) for the provider-specific parameters and requirements.

