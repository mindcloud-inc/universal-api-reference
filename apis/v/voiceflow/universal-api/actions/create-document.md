# Voiceflow: Create Document

Creates a knowledge base document in Voiceflow.

```
POST https://connect.mindcloud.co/v1/universal/voiceflow/latest/actions/create-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Voiceflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/voiceflow/latest/actions/create-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/voiceflow/latest/actions/create-document', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data` | object | yes | Document source payload nested under the top-level data field. Example: `[object Object]`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `maxChunkSize` | number | no | Chunk size in tokens. Example: `1000`. |
| `overwrite` | boolean | no | Overwrite an existing document with the same name. |
| `markdownConversion` | boolean | no | Convert HTML to markdown before chunking. |
| `llmBasedChunks` | boolean | no | Use LLM-based chunking. |
| `llmGeneratedQ` | boolean | no | Prepend LLM-generated retrieval questions to chunks. |
| `llmContentSummarization` | boolean | no | Summarize content with an LLM before indexing. |
| `llmPrependContext` | boolean | no | Prepend LLM-generated chunk context. |
| `llmVision` | boolean | no | Use vision support when extracting document content. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Created document payload. |

## Native endpoint

Through the native Voiceflow API, this operation is `POST https://realtime-api.voiceflow.com/v1alpha1/public/knowledge-base/document` (base URL `https://general-runtime.voiceflow.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-document.md) for the provider-specific parameters and requirements.

