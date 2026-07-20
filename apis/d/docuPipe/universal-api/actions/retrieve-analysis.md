# DocuPipe: Retrieve Analysis

Retrieves an analysis from DocuPipe.

```
GET https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/retrieve-analysis
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocuPipe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/retrieve-analysis?connectionId=$CONNECTION_ID&analysisId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "analysisId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/retrieve-analysis?${params}`, {
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
| `analysisId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "analysisId": "string",
      "data": [
        {}
      ],
      "dataset": "string",
      "documentIds": [
        "string"
      ],
      "filename": "Ava Chen",
      "jobId": "string",
      "numDocs": 1,
      "pages": [
        1
      ],
      "schemaId": "string",
      "timestamp": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `analysisId` | string | Unique identifier of the analysis object. |
| `data` | array<object> | List of questions and answers for the analysis, along with confidence and citations. |
| `dataset` | string | Dataset which defines what documents are included in the analysis. |
| `documentIds` | array<string> | List of document IDs that were analyzed. |
| `filename` | string | Name of the file that was analyzed, if there is only a single document. |
| `jobId` | string | Unique identifier of the job that created the analysis. |
| `numDocs` | number | Number of documents analyzed. |
| `pages` | array<number> | List of page numbers to analyze. If none, all pages are analyzed. Only applies for single document. |
| `schemaId` | string | Unique identifier of the schema used to fetch standardizations for querying. |
| `timestamp` | string | Timestamp of the analysis job. |

## Native endpoint

Through the native DocuPipe API, this operation is `GET /analysis/:analysisId` (base URL `https://app.docupipe.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-analysis.md) for the provider-specific parameters and requirements.

