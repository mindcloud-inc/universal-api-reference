# Allscreenshots: Get Screenshot Job Status

Retrieves the status of an async screenshot job in Allscreenshots.

```
GET https://connect.mindcloud.co/v1/universal/allscreenshots/latest/actions/get-screenshot-job-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Allscreenshots `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/allscreenshots/latest/actions/get-screenshot-job-status?connectionId=$CONNECTION_ID&job_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "job_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/allscreenshots/latest/actions/get-screenshot-job-status?${params}`, {
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
| `job_id` | string | yes | The async screenshot job to inspect. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "completedAt": "2026-05-07T12:00:00.000Z",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "errorCode": "string",
      "errorMessage": "string",
      "expiresAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "metadata": {
        "format": "string",
        "height": 1,
        "size": 1,
        "width": 1
      },
      "outputs": {
        "markdown": {
          "contentType": "string",
          "resultUrl": "https://example.com",
          "size": 1,
          "storageUrl": "https://example.com",
          "type": "string"
        },
        "screenshot": {
          "contentType": "string",
          "resultUrl": "https://example.com",
          "size": 1,
          "storageUrl": "https://example.com",
          "type": "string"
        }
      },
      "resultUrl": "https://example.com",
      "startedAt": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "storageUrl": "https://example.com",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `completedAt` | date |  |
| `createdAt` | date |  |
| `errorCode` | string |  |
| `errorMessage` | string |  |
| `expiresAt` | date |  |
| `id` | string |  |
| `metadata.format` | string |  |
| `metadata.height` | number |  |
| `metadata.size` | number |  |
| `metadata.width` | number |  |
| `outputs.markdown.contentType` | string |  |
| `outputs.markdown.resultUrl` | string |  |
| `outputs.markdown.size` | number |  |
| `outputs.markdown.storageUrl` | string |  |
| `outputs.markdown.type` | string |  |
| `outputs.screenshot.contentType` | string |  |
| `outputs.screenshot.resultUrl` | string |  |
| `outputs.screenshot.size` | number |  |
| `outputs.screenshot.storageUrl` | string |  |
| `outputs.screenshot.type` | string |  |
| `resultUrl` | string |  |
| `startedAt` | date |  |
| `status` | string |  |
| `storageUrl` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Allscreenshots API, this operation is `GET /v1/screenshots/jobs/:jobId` (base URL `https://api.allscreenshots.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-screenshot-job-status.md) for the provider-specific parameters and requirements.

