# Ainoflow Convert: Get Job Status

Retrieves conversion job status and download URLs from Ainoflow Convert.

```
GET https://connect.mindcloud.co/v1/universal/ainoflowConvert/latest/actions/get-job-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ainoflow Convert `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ainoflowConvert/latest/actions/get-job-status?connectionId=$CONNECTION_ID&jobId=00000000-0000-0000-0000-000000000000" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "00000000-0000-0000-0000-000000000000"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ainoflowConvert/latest/actions/get-job-status?${params}`, {
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
| `jobId` | string | yes | Job ID returned from a submit action. Default: `00000000-0000-0000-0000-000000000000`. Example: `00000000-0000-0000-0000-000000000000`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "completedAt": "string",
      "createdAt": "string",
      "expiryAt": "string",
      "files": [
        {
          "models": "string",
          "text": {
            "expiration": "string",
            "url": "https://example.com"
          }
        }
      ],
      "id": "string",
      "models": "string",
      "processingTimeInSeconds": 1,
      "reference": "string",
      "responseMode": "string",
      "startedAt": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `completedAt` | string |  |
| `createdAt` | string |  |
| `expiryAt` | string |  |
| `files` | array<object> |  |
| `files[].models` | string |  |
| `files[].text.expiration` | string |  |
| `files[].text.url` | string |  |
| `id` | string |  |
| `models` | string |  |
| `processingTimeInSeconds` | number |  |
| `reference` | string |  |
| `responseMode` | string |  |
| `startedAt` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Ainoflow Convert API, this operation is `GET /api/v1/convert/jobs/:jobId` (base URL `https://api.ainoflow.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-job-status.md) for the provider-specific parameters and requirements.

