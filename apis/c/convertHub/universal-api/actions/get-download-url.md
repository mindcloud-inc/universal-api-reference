# ConvertHub: Get Download URL

Retrieves a converted file URL or base64 content from ConvertHub.

```
GET https://connect.mindcloud.co/v1/universal/convertHub/latest/actions/get-download-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ConvertHub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/convertHub/latest/actions/get-download-url?connectionId=$CONNECTION_ID&jobId=job_123e4567-e89b-12d3-a456-426614174000" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "job_123e4567-e89b-12d3-a456-426614174000"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/convertHub/latest/actions/get-download-url?${params}`, {
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
| `format` | list | no | Set to base64 to return the file content as a base64-encoded string instead of a download URL. One of: `base64`. Example: `base64`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "download_url": "https://example.com",
      "expires_at": "string",
      "file_base64": "string",
      "file_size": 1,
      "filename": "Ava Chen",
      "format": "string",
      "job_id": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `download_url` | string |  |
| `expires_at` | string |  |
| `file_base64` | string |  |
| `file_size` | number |  |
| `filename` | string |  |
| `format` | string |  |
| `job_id` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native ConvertHub API, this operation is `GET /v2/jobs/:jobId/download` (base URL `https://api.converthub.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-download-url.md) for the provider-specific parameters and requirements.

