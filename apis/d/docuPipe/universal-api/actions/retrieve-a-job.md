# DocuPipe: Retrieve a Job

Retrieves a job from DocuPipe.

```
GET https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/retrieve-a-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocuPipe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/retrieve-a-job?connectionId=$CONNECTION_ID&jobId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/retrieve-a-job?${params}`, {
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
| `jobId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "analysisId": "string",
      "assignedClassIds": [
        "string"
      ],
      "classIds": [
        "string"
      ],
      "classifyJobIds": [
        "string"
      ],
      "client": "string",
      "credits": 1,
      "dataset": "string",
      "details": [
        {}
      ],
      "displayMode": "string",
      "documentCount": 1,
      "documentId": "string",
      "documentIds": [
        "string"
      ],
      "effortLevel": "string",
      "errorMessage": "string",
      "feedback": "string",
      "fileExtension": "string",
      "filename": "Ava Chen",
      "filenamePrefix": "Ava Chen",
      "fileType": "string",
      "guidelines": "string",
      "includeUnknown": true,
      "instructions": "string",
      "jobId": "string",
      "jobType": "string",
      "language": "string",
      "matchCandidates": [
        "string"
      ],
      "matchedDocumentIds": [
        "string"
      ],
      "matchedStandardizationIds": [
        "string"
      ],
      "multiClass": true,
      "newDocumentId": "string",
      "newDocumentIds": [
        "string"
      ],
      "newSchemaId": "string",
      "numNewDocuments": 1,
      "numPages": 1,
      "pageCount": 1,
      "pages": [
        1
      ],
      "pagesParsed": [
        1
      ],
      "parseVersion": 1,
      "processingMethod": "string",
      "processingTime": 1,
      "progress": 1,
      "query": "string",
      "questions": [
        "string"
      ],
      "releaseVersion": 1,
      "reviewId": "string",
      "reviewInstructions": "string",
      "schemaId": "string",
      "schemaName": "Ava Chen",
      "splitMode": "string",
      "standardizationId": "string",
      "standardizationIds": [
        "string"
      ],
      "standardizationJobIds": [
        "string"
      ],
      "standardizationMode": "string",
      "standardizeUsingSchema": true,
      "status": "string",
      "stdVersion": 1,
      "timestamp": "2026-05-07T12:00:00.000Z",
      "useMetadata": true,
      "workflowId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `analysisId` | string |  |
| `assignedClassIds` | array<string> |  |
| `classIds` | array<string> |  |
| `classifyJobIds` | array<string> |  |
| `client` | string |  |
| `credits` | number | Number of credits used by the operation. |
| `dataset` | string | Name of the dataset the document belongs to. |
| `details` | array<object> |  |
| `displayMode` | string |  |
| `documentCount` | number |  |
| `documentId` | string | Unique identifier of the document. |
| `documentIds` | array<string> |  |
| `effortLevel` | string |  |
| `errorMessage` | string | Error message if the job failed. |
| `feedback` | string |  |
| `fileExtension` | string |  |
| `filename` | string |  |
| `filenamePrefix` | string |  |
| `fileType` | string |  |
| `guidelines` | string |  |
| `includeUnknown` | boolean |  |
| `instructions` | string |  |
| `jobId` | string | Unique identifier of the job. |
| `jobType` | string |  |
| `language` | string |  |
| `matchCandidates` | array<string> |  |
| `matchedDocumentIds` | array<string> |  |
| `matchedStandardizationIds` | array<string> |  |
| `multiClass` | boolean |  |
| `newDocumentId` | string |  |
| `newDocumentIds` | array<string> |  |
| `newSchemaId` | string |  |
| `numNewDocuments` | number |  |
| `numPages` | number |  |
| `pageCount` | number | Number of pages used to create the schema. |
| `pages` | array<number> |  |
| `pagesParsed` | array<number> |  |
| `parseVersion` | number |  |
| `processingMethod` | string |  |
| `processingTime` | number | Processing time in seconds. |
| `progress` | number | Job progress percentage (0-100). Currently used by V3 standardization jobs. |
| `query` | string |  |
| `questions` | array<string> |  |
| `releaseVersion` | number |  |
| `reviewId` | string |  |
| `reviewInstructions` | string |  |
| `schemaId` | string |  |
| `schemaName` | string |  |
| `splitMode` | string |  |
| `standardizationId` | string |  |
| `standardizationIds` | array<string> |  |
| `standardizationJobIds` | array<string> |  |
| `standardizationMode` | string |  |
| `standardizeUsingSchema` | boolean |  |
| `status` | string | Current status of the job. |
| `stdVersion` | number |  |
| `timestamp` | date | Timestamp of the job creation. |
| `useMetadata` | boolean |  |
| `workflowId` | string |  |

## Native endpoint

Through the native DocuPipe API, this operation is `GET /job/:jobId` (base URL `https://app.docupipe.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-a-job.md) for the provider-specific parameters and requirements.

