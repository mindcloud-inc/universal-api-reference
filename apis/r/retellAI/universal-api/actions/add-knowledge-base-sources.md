# Retell AI: Add Knowledge Base Sources

Adds sources to a knowledge base in Retell AI.

```
PUT https://connect.mindcloud.co/v1/universal/retellAI/latest/actions/add-knowledge-base-sources
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Retell AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/retellAI/latest/actions/add-knowledge-base-sources" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "knowledgeBaseId": "string",
  "knowledgeBaseTexts[].title": "string",
  "knowledgeBaseTexts[].text": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/retellAI/latest/actions/add-knowledge-base-sources', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "knowledgeBaseId": "string",
    "knowledgeBaseTexts[].title": "string",
    "knowledgeBaseTexts[].text": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `knowledgeBaseFiles[]` | array<file> | no | Files to add to the knowledge base. Limit to 25 files, where each file is limited to 50MB. |
| `knowledgeBaseId` | string | yes |  |
| `knowledgeBaseTexts[]` | array<object> | no | Texts to add to the knowledge base. |
| `knowledgeBaseUrls[]` | array<string> | no | URLs to be scraped and added to the knowledge base. Must be valid urls. |
| `knowledgeBaseTexts[]` | array<object> | no | Texts to add to the knowledge base. |
| `knowledgeBaseTexts[]` | array<object> | no | Texts to add to the knowledge base. |
| `knowledgeBaseTexts[].title` | string | yes | Title of the text. |
| `knowledgeBaseTexts[].text` | string | yes | Text to add to the knowledge base. |
| `knowledgeBaseFiles[]` | array<file> | no | Files to add to the knowledge base. Limit to 25 files, where each file is limited to 50MB. |
| `knowledgeBaseFiles[]` | array<file> | no | Files to add to the knowledge base. Limit to 25 files, where each file is limited to 50MB. |
| `knowledgeBaseUrls[]` | array<string> | no | URLs to be scraped and added to the knowledge base. Must be valid urls. |
| `knowledgeBaseUrls[]` | array<string> | no | URLs to be scraped and added to the knowledge base. Must be valid urls. |

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

Through the native Retell AI API, this operation is `POST /add-knowledge-base-sources/{knowledge_base_id}` (base URL `https://api.retellai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-knowledge-base-sources.md) for the provider-specific parameters and requirements.

