# Mindee: Start Split Job From URL

Creates a new split job in Mindee from a URL.

```
POST https://connect.mindcloud.co/v1/universal/mindee/latest/actions/start-split-job-from-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mindee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mindee/latest/actions/start-split-job-from-url" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "modelId": "string",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mindee/latest/actions/start-split-job-from-url', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "modelId": "string",
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `modelId` | string | yes | Model ID to use for the inference. |
| `url` | string | yes | Download the file from a public HTTPS URL. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "job": {
        "created_at": "2026-05-07T12:00:00.000Z",
        "filename": "Ava Chen",
        "id": "string",
        "model_id": "string",
        "polling_url": "https://example.com",
        "status": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `job.created_at` | date |  |
| `job.filename` | string |  |
| `job.id` | string |  |
| `job.model_id` | string |  |
| `job.polling_url` | string |  |
| `job.status` | string |  |

## Native endpoint

Through the native Mindee API, this operation is `POST /v2/products/split/enqueue` (base URL `https://api-v2.mindee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/start-split-job-from-url.md) for the provider-specific parameters and requirements.

