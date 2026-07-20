# DocuPipe: List Jobs

Retrieves jobs from DocuPipe.

```
GET https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/list-jobs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocuPipe `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/list-jobs?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/list-jobs?${params}`, {
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
| `startDate` | string | no |  |
| `endDate` | string | no |  |
| `status` | string | no |  |
| `jobType` | string | no |  |
| `schemaId` | string | no |  |
| `documentId` | string | no |  |
| `newDocumentId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "credits": 1,
      "dataset": "string",
      "documentId": "string",
      "errorMessage": "string",
      "jobId": "string",
      "jobType": "string",
      "processingTime": 1,
      "progress": 1,
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
| `credits` | number | Number of credits used by the operation. |
| `dataset` | string | Name of the dataset the document belongs to. |
| `documentId` | string | Unique identifier of the document. |
| `errorMessage` | string | Error message if the job failed. |
| `jobId` | string | Unique identifier of the job. |
| `jobType` | string | Type of the job. |
| `processingTime` | number | Processing time in seconds. |
| `progress` | number | Job progress percentage (0-100). Currently used by V3 standardization jobs. |
| `status` | string | Current status of the job. |
| `timestamp` | date | Timestamp of the job creation. |

## Native endpoint

Through the native DocuPipe API, this operation is `GET /jobs` (base URL `https://app.docupipe.ai`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-jobs.md) for the provider-specific parameters and requirements.

