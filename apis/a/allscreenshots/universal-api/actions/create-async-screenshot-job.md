# Allscreenshots: Create Async Screenshot Job

Creates a new async screenshot job in Allscreenshots.

```
POST https://connect.mindcloud.co/v1/universal/allscreenshots/latest/actions/create-async-screenshot-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Allscreenshots `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/allscreenshots/latest/actions/create-async-screenshot-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/allscreenshots/latest/actions/create-async-screenshot-job', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes | The webpage URL to capture asynchronously. |
| `format` | string | no | Output format such as png, jpeg, webp, or pdf. |
| `full_page` | boolean | no | Capture the full scrollable page instead of the visible viewport. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `response_type` | string | no | How the finished job result should be returned. |
| `webhook_url` | string | no | Optional URL to notify when the async job completes. |
| `webhook_secret` | string | no | Optional secret used to sign webhook deliveries. |
| `outputs[]` | array<object> | no | Optional multi-output extraction configuration. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "status": "string",
      "statusUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `id` | string |  |
| `status` | string |  |
| `statusUrl` | string |  |

## Native endpoint

Through the native Allscreenshots API, this operation is `POST /v1/screenshots/async` (base URL `https://api.allscreenshots.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-async-screenshot-job.md) for the provider-specific parameters and requirements.

