# DocuPipe: List Analyses

Retrieves analyses from DocuPipe.

```
GET https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/list-analyses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocuPipe `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/list-analyses?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/list-analyses?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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

Through the native DocuPipe API, this operation is `GET /analyses` (base URL `https://app.docupipe.ai`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-analyses.md) for the provider-specific parameters and requirements.

