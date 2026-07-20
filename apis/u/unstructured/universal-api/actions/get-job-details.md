# Unstructured: Get Job Details

Retrieves job details from Unstructured.

```
GET https://connect.mindcloud.co/v1/universal/unstructured/latest/actions/get-job-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Unstructured `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/unstructured/latest/actions/get-job-details?connectionId=$CONNECTION_ID&jobId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/unstructured/latest/actions/get-job-details?${params}`, {
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
| `jobId` | string | yes | The job ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "completedAt": "string",
      "completedFiles": 1,
      "createdAt": "string",
      "failedFiles": 1,
      "id": "string",
      "outputNodeFiles": [
        [
          {}
        ]
      ],
      "startedAt": "string",
      "status": "string",
      "totalFiles": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `completedAt` | string | Processing completion timestamp. |
| `completedFiles` | number | Completed file count. |
| `createdAt` | string | Creation timestamp. |
| `failedFiles` | number | Failed file count. |
| `id` | string | Job ID. |
| `outputNodeFiles[]` | array<object> | Output node files. |
| `startedAt` | string | Processing start timestamp. |
| `status` | string | Job status. |
| `totalFiles` | number | Total number of files in the job. |

## Native endpoint

Through the native Unstructured API, this operation is `GET /jobs/:job_id/details` (base URL `https://platform.unstructuredapp.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-job-details.md) for the provider-specific parameters and requirements.

