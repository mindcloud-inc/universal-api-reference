# Cohere: Create Embed Job

Creates a new embed job in Cohere.

```
POST https://connect.mindcloud.co/v1/universal/cohere/latest/actions/create-embed-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cohere `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cohere/latest/actions/create-embed-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cohere/latest/actions/create-embed-job', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "inputDatasetId": "string",
      "jobId": "string",
      "meta": {},
      "model": "string",
      "name": "Ava Chen",
      "outputDatasetId": "string",
      "status": "string",
      "truncate": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `inputDatasetId` | string |  |
| `jobId` | string |  |
| `meta` | object |  |
| `model` | string |  |
| `name` | string |  |
| `outputDatasetId` | string |  |
| `status` | string |  |
| `truncate` | string |  |

## Native endpoint

Through the native Cohere API, this operation is `POST /v1/embed-jobs` (base URL `https://api.cohere.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-embed-job.md) for the provider-specific parameters and requirements.

