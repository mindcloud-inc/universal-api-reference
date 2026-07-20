# Allscreenshots: Get Bulk Job Status

Retrieves the status of a bulk screenshot job in Allscreenshots.

```
GET https://connect.mindcloud.co/v1/universal/allscreenshots/latest/actions/get-bulk-job-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Allscreenshots `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/allscreenshots/latest/actions/get-bulk-job-status?connectionId=$CONNECTION_ID&bulk_job_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "bulk_job_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/allscreenshots/latest/actions/get-bulk-job-status?${params}`, {
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
| `bulk_job_id` | string | yes | The bulk screenshot job to inspect. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "completedAt": "2026-05-07T12:00:00.000Z",
      "completedJobs": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "failedJobs": 1,
      "id": "string",
      "jobs": [
        {
          "completedAt": "2026-05-07T12:00:00.000Z",
          "createdAt": "2026-05-07T12:00:00.000Z",
          "errorCode": "string",
          "errorMessage": "string",
          "fileSize": 1,
          "format": "string",
          "height": 1,
          "id": "string",
          "renderTimeMs": 1,
          "resultUrl": "https://example.com",
          "status": "string",
          "storageUrl": "https://example.com",
          "url": "https://example.com",
          "width": 1
        }
      ],
      "progress": 1,
      "status": "string",
      "totalJobs": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `completedAt` | date |  |
| `completedJobs` | number |  |
| `createdAt` | date |  |
| `failedJobs` | number |  |
| `id` | string |  |
| `jobs[].completedAt` | date |  |
| `jobs[].createdAt` | date |  |
| `jobs[].errorCode` | string |  |
| `jobs[].errorMessage` | string |  |
| `jobs[].fileSize` | number |  |
| `jobs[].format` | string |  |
| `jobs[].height` | number |  |
| `jobs[].id` | string |  |
| `jobs[].renderTimeMs` | number |  |
| `jobs[].resultUrl` | string |  |
| `jobs[].status` | string |  |
| `jobs[].storageUrl` | string |  |
| `jobs[].url` | string |  |
| `jobs[].width` | number |  |
| `progress` | number |  |
| `status` | string |  |
| `totalJobs` | number |  |

## Native endpoint

Through the native Allscreenshots API, this operation is `GET /v1/screenshots/bulk/:bulkJobId` (base URL `https://api.allscreenshots.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-bulk-job-status.md) for the provider-specific parameters and requirements.

