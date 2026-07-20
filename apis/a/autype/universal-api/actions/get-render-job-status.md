# Autype: Get Render Job Status

Retrieves render job status from Autype.

```
GET https://connect.mindcloud.co/v1/universal/autype/latest/actions/get-render-job-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Autype `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/autype/latest/actions/get-render-job-status?connectionId=$CONNECTION_ID&jobId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/autype/latest/actions/get-render-job-status?${params}`, {
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
      "completedAt": "2026-05-07T12:00:00.000Z",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "downloadUrl": "https://example.com",
      "error": "string",
      "filename": "Ava Chen",
      "format": "string",
      "jobId": "string",
      "progress": 1,
      "status": "string"
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
| `downloadUrl` | string |  |
| `error` | string |  |
| `filename` | string |  |
| `format` | string |  |
| `jobId` | string |  |
| `progress` | number |  |
| `status` | string |  |

## Native endpoint

Through the native Autype API, this operation is `GET /render/{jobId}` (base URL `https://api.autype.com/api/v1/dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-render-job-status.md) for the provider-specific parameters and requirements.

