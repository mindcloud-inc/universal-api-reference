# DocMaker: Get Job Status

Retrieves job status from DocMaker.

```
GET https://connect.mindcloud.co/v1/universal/docMaker/latest/actions/get-job-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocMaker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docMaker/latest/actions/get-job-status?connectionId=$CONNECTION_ID&jobId=7f901fa7-4cb5-46d3-9a83-c9f5a0c860a2" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "7f901fa7-4cb5-46d3-9a83-c9f5a0c860a2"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docMaker/latest/actions/get-job-status?${params}`, {
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
| `jobId` | string | yes | The unique identifier of the DocMaker job. Example: `7f901fa7-4cb5-46d3-9a83-c9f5a0c860a2`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": 1,
      "jobId": "string",
      "jsonRequest": "string",
      "name": "Ava Chen",
      "remaining_credits": 1,
      "result_file": "string",
      "route": "string",
      "status": "string",
      "status_code": 1,
      "updatedAt": 1,
      "userId": "string",
      "workflowID": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | number | When the job was created. |
| `jobId` | string | The DocMaker job identifier. |
| `jsonRequest` | string | The request payload DocMaker stored for the job. |
| `name` | string | The output file name for the job. |
| `remaining_credits` | number | Remaining DocMaker credits after the job. |
| `result_file` | string | The generated file URL when available. |
| `route` | string | The DocMaker endpoint route that created the job. |
| `status` | string | The current DocMaker job status. |
| `status_code` | number | The HTTP-like status code reported by DocMaker. |
| `updatedAt` | number | When the job was last updated. |
| `userId` | string | The DocMaker user identifier for the job owner. |
| `workflowID` | string | The DocMaker workflow identifier for the job. |

## Native endpoint

Through the native DocMaker API, this operation is `GET /jobs/:jobId` (base URL `https://api.v2.docmaker.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-job-status.md) for the provider-specific parameters and requirements.

