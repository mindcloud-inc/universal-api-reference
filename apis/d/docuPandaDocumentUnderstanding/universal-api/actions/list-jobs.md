# DocuPanda - Document Understanding: List Jobs

Retrieves jobs from DocuPanda.

```
GET https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/list-jobs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocuPanda - Document Understanding `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/list-jobs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/list-jobs?${params}`, {
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
| `start_date` | string | no |  |
| `end_date` | string | no |  |
| `status` | string | no |  |
| `job_type` | string | no |  |
| `schema_id` | string | no |  |
| `document_id` | string | no |  |
| `new_document_id` | string | no |  |
| `limit` | number | no |  |
| `offset` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dataset": "string",
      "documentId": "string",
      "jobId": "string",
      "jobType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dataset` | string | Name of the dataset the document belongs to. |
| `documentId` | string | Unique identifier of the document. |
| `jobId` | string | Unique identifier of the job. |
| `jobType` | string | Type of the job. |

## Native endpoint

Through the native DocuPanda - Document Understanding API, this operation is `GET /jobs` (base URL `https://app.docupipe.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-jobs.md) for the provider-specific parameters and requirements.

