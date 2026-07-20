# DocuPipe: Analyze Data

Analyzes structured data in DocuPipe.

```
POST https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/analyze-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocuPipe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/analyze-data" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "questions[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/analyze-data', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "questions[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `documentIds[]` | array<string> | no | List of document IDs to analyze. If both dataset and documentIds are provided, we take the intersection of the two. |
| `dataset` | string | no | Dataset which defines what documents are included in the analysis. If both dataset and documentIds are provided, we take the intersection of the two. |
| `schemaId` | string | no | Unique identifier of the schema to be used for the analysis. If provided, only those documents with a valid standardization under this schema will be included in the analysis. |
| `questions[]` | array<string> | yes | List of questions to be answered. |
| `instructions` | string | no | Global instructions to provide additional guidelines or context to the AI when answering the questions. |

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

Through the native DocuPipe API, this operation is `POST /analyze/data` (base URL `https://app.docupipe.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/analyze-data.md) for the provider-specific parameters and requirements.

