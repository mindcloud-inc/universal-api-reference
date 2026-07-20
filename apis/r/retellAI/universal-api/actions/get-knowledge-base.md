# Retell AI: Get Knowledge Base

Retrieves a knowledge base from Retell AI.

```
GET https://connect.mindcloud.co/v1/universal/retellAI/latest/actions/get-knowledge-base
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Retell AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/retellAI/latest/actions/get-knowledge-base?connectionId=$CONNECTION_ID&knowledgeBaseId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "knowledgeBaseId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/retellAI/latest/actions/get-knowledge-base?${params}`, {
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
| `knowledgeBaseId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "enableAutoRefresh": true,
      "knowledgeBaseId": "string",
      "knowledgeBaseName": "Ava Chen",
      "knowledgeBaseSources": [
        {
          "filename": "Ava Chen",
          "fileUrl": "https://example.com",
          "sourceId": "string",
          "type": "string"
        }
      ],
      "lastRefreshedTimestamp": 1,
      "maxChunkSize": 1,
      "minChunkSize": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `enableAutoRefresh` | boolean | Whether to enable auto refresh for the knowledge base urls. If set to true, will retrieve the data from the specified url every 12 hours. |
| `knowledgeBaseId` | string | Unique id of the knowledge base. |
| `knowledgeBaseName` | string | Name of the knowledge base. Must be less than 40 characters. |
| `knowledgeBaseSources` | array<object> | Sources of the knowledge base. Will be populated after the processing is done (when status is "complete"). |
| `knowledgeBaseSources[].filename` | string | Filename of the document. |
| `knowledgeBaseSources[].fileUrl` | string | URL of the document stored. |
| `knowledgeBaseSources[].sourceId` | string | Unique id of the knowledge base source. |
| `knowledgeBaseSources[].type` | string | Type of the knowledge base source. Allowed values: document. |
| `lastRefreshedTimestamp` | number | Last refreshed timestamp (milliseconds since epoch). Only applicable when enable_auto_refresh is true. |
| `maxChunkSize` | number | Maximum number of characters per chunk when splitting knowledge base content. |
| `minChunkSize` | number | Minimum number of characters per chunk. Chunks smaller than this are merged with adjacent chunks. |
| `status` | string | Status of the knowledge base. When it's created and being processed, it's "in_progress". When the processing is done, it's "complete". When there's an error in processing, it's "error". When it is during kb updating, it's "refreshing_in_progress". Allowed values: in_progress, complete, error, refreshing_in_progress. |

## Native endpoint

Through the native Retell AI API, this operation is `GET /get-knowledge-base/{knowledge_base_id}` (base URL `https://api.retellai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-knowledge-base.md) for the provider-specific parameters and requirements.

