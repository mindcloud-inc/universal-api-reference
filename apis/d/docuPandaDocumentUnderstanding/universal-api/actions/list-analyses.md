# DocuPanda - Document Understanding: List Analyses

Retrieves analyses from DocuPanda.

```
GET https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/list-analyses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocuPanda - Document Understanding `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/list-analyses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/list-analyses?${params}`, {
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
| `limit` | number | no | The maximum number of analyses to return. maximum is 20 |
| `offset` | number | no | The number of analyses to skip (to paginate through the data) |

## Response

```json
{
  "success": true,
  "data": [
    {
      "analysisId": "string",
      "documentIds": [
        "string"
      ],
      "filename": "Ava Chen",
      "jobId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `analysisId` | string | Unique identifier of the analysis object. |
| `documentIds` | array<string> | List of document IDs that were analyzed. |
| `filename` | string | Name of the file that was analyzed, if there is only a single document. |
| `jobId` | string | Unique identifier of the job that created the analysis. |

## Native endpoint

Through the native DocuPanda - Document Understanding API, this operation is `GET /analyses` (base URL `https://app.docupipe.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-analyses.md) for the provider-specific parameters and requirements.

