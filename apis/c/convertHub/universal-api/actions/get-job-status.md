# ConvertHub: Get Job Status

Retrieves a conversion job's status from ConvertHub.

```
GET https://connect.mindcloud.co/v1/universal/convertHub/latest/actions/get-job-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ConvertHub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/convertHub/latest/actions/get-job-status?connectionId=$CONNECTION_ID&jobId=job_123e4567-e89b-12d3-a456-426614174000" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "job_123e4567-e89b-12d3-a456-426614174000"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/convertHub/latest/actions/get-job-status?${params}`, {
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
| `jobId` | string | yes | Example: `job_123e4567-e89b-12d3-a456-426614174000`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "string",
      "job_id": "string",
      "links": {
        "cancel": "https://example.com",
        "download": "https://example.com",
        "status": "https://example.com"
      },
      "message": "string",
      "metadata": {
        "project_id": "string"
      },
      "processing_time": "string",
      "result": {
        "download_url": "https://example.com",
        "expires_at": "string",
        "file_size": 1,
        "format": "string"
      },
      "source_format": "string",
      "status": "string",
      "success": true,
      "target_format": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string |  |
| `job_id` | string |  |
| `links` | object |  |
| `links.cancel` | string |  |
| `links.download` | string |  |
| `links.status` | string |  |
| `message` | string |  |
| `metadata` | object |  |
| `metadata.project_id` | string |  |
| `processing_time` | string |  |
| `result` | object |  |
| `result.download_url` | string |  |
| `result.expires_at` | string |  |
| `result.file_size` | number |  |
| `result.format` | string |  |
| `source_format` | string |  |
| `status` | string |  |
| `success` | boolean |  |
| `target_format` | string |  |

## Native endpoint

Through the native ConvertHub API, this operation is `GET /v2/jobs/:jobId` (base URL `https://api.converthub.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-job-status.md) for the provider-specific parameters and requirements.

