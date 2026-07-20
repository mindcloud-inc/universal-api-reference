# DocuPanda - Document Understanding: Classify Documents

Creates document classifications in DocuPanda.

```
POST https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/post-classify-batch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocuPanda - Document Understanding `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/post-classify-batch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "documentIds": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/post-classify-batch', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "documentIds": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `classIds` | list<string> | no | List of class IDs to use for classification |
| `displayMode` | string | no |  |
| `documentIds` | list<string> | yes | List of document IDs to classify |
| `includeUnknown` | boolean | no | Whether to include the 'unknown' class in the classification (only relevant if multiClass is false) |
| `instructions` | string | no | Instructions for the AI on how to classify the documents |
| `multiClass` | boolean | no | Whether to allow multiple classifications per document |

## Response

```json
{
  "success": true,
  "data": [
    {
      "classificationJobIds": [
        "string"
      ],
      "documentCount": 1,
      "jobId": "string",
      "pageCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `classificationJobIds` | array<string> | List of individual job IDs for each document's classify job |
| `documentCount` | number | Number of documents processed |
| `jobId` | string | ID of the batch classification job |
| `pageCount` | number | Number of pages processed |

## Native endpoint

Through the native DocuPanda - Document Understanding API, this operation is `POST /classify/batch` (base URL `https://app.docupipe.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/post-classify-batch.md) for the provider-specific parameters and requirements.

