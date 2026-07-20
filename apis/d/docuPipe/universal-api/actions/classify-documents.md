# DocuPipe: Classify Documents

Classifies documents in DocuPipe.

```
POST https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/classify-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocuPipe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/classify-documents" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "documentIds[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/classify-documents', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "documentIds[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `documentIds[]` | array<string> | yes | List of document IDs to classify |
| `classIds[]` | array<string> | no | List of class IDs to use for classification |
| `multiClass` | boolean | no | Whether to allow multiple classifications per document Default: `false`. |
| `includeUnknown` | boolean | no | Whether to include the 'unknown' class in the classification (only relevant if multiClass is false) Default: `true`. |
| `instructions` | string | no | Instructions for the AI on how to classify the documents |
| `displayMode` | list | no | *Advanced Feature* Mode of display to run. The options are: `auto`: AI decides how to display the document (default) `spatial`: Display text spatially, as it appears in the document `sections`: Display text from top to bottom as sections, with tables appearing as markdown `image`: Display as an image. One of: `auto`, `image`, `sections`, `spatial`. |

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
      "pageCount": 1,
      "status": "string",
      "timestamp": "2026-05-07T12:00:00.000Z"
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
| `status` | string | Status of the batch classification job |
| `timestamp` | date | Timestamp of the classification job |

## Native endpoint

Through the native DocuPipe API, this operation is `POST /classify/batch` (base URL `https://app.docupipe.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/classify-documents.md) for the provider-specific parameters and requirements.

