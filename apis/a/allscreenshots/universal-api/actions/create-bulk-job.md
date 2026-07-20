# Allscreenshots: Create Bulk Job

Creates a bulk screenshot job for multiple URLs in Allscreenshots.

```
POST https://connect.mindcloud.co/v1/universal/allscreenshots/latest/actions/create-bulk-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Allscreenshots `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/allscreenshots/latest/actions/create-bulk-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "urls[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/allscreenshots/latest/actions/create-bulk-job', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "urls[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `urls[]` | array<object> | yes | The list of capture requests to include in the bulk job. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `defaults` | object | no | Shared screenshot options applied to every URL unless overridden. |
| `webhook_url` | string | no | Optional URL to notify when the bulk job completes. |
| `webhook_secret` | string | no | Optional secret used to sign webhook deliveries. |

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
          "errorCode": "string",
          "errorMessage": "string",
          "id": "string",
          "resultUrl": "https://example.com",
          "status": "string",
          "url": "https://example.com"
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
| `jobs[].errorCode` | string |  |
| `jobs[].errorMessage` | string |  |
| `jobs[].id` | string |  |
| `jobs[].resultUrl` | string |  |
| `jobs[].status` | string |  |
| `jobs[].url` | string |  |
| `progress` | number |  |
| `status` | string |  |
| `totalJobs` | number |  |

## Native endpoint

Through the native Allscreenshots API, this operation is `POST /v1/screenshots/bulk` (base URL `https://api.allscreenshots.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-bulk-job.md) for the provider-specific parameters and requirements.

