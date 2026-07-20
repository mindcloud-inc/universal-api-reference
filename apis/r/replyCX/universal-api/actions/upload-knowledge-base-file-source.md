# ReplyCX: Upload Knowledge Base File Source



```
POST https://connect.mindcloud.co/v1/universal/replyCX/latest/actions/upload-knowledge-base-file-source
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ReplyCX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/replyCX/latest/actions/upload-knowledge-base-file-source" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "knowledgeBaseId": 1,
  "q1": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/replyCX/latest/actions/upload-knowledge-base-file-source', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "knowledgeBaseId": 1,
    "q1": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `knowledgeBaseId` | number | yes |  |
| `q1` | file | yes | File to upload as one knowledge-base source field. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ReplyCX API returns.

## Native endpoint

Through the native ReplyCX API, this operation is `POST /api/v1/ai/knowledge-base/:knowledge_base_id/upload/sources` (base URL `https://api.reply.cx`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-knowledge-base-file-source.md) for the provider-specific parameters and requirements.

