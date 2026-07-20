# DocuPanda - Document Understanding: Analyze Data

Creates a batch analysis in DocuPanda.

```
POST https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/post-analyze-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocuPanda - Document Understanding `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/post-analyze-data" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "questions": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/post-analyze-data', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "questions": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `dataset` | string | no | Dataset which defines what documents are included in the analysis. If both dataset and documentIds are provided, we take the intersection of the two. |
| `documentIds` | list<string> | no | List of document IDs to analyze. If both dataset and documentIds are provided, we take the intersection of the two. |
| `instructions` | string | no | Global instructions to provide additional guidelines or context to the AI when answering the questions. |
| `questions` | list<string> | yes | List of questions to be answered. |
| `schemaId` | string | no | Unique identifier of the schema to be used for the analysis. If provided, only those documents with a valid standardization under this schema will be included in the analysis. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "analysisId": "string",
      "jobId": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `analysisId` | string | Unique identifier for the analysis. |
| `jobId` | string | Unique identifier for the submitted job. |
| `success` | boolean | Whether the job was successful launched or not. |

## Native endpoint

Through the native DocuPanda - Document Understanding API, this operation is `POST /analyze/data` (base URL `https://app.docupipe.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/post-analyze-data.md) for the provider-specific parameters and requirements.

