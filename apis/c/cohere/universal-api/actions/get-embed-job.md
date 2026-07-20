# Cohere: Get Embed Job

Retrieves an embed job from Cohere.

```
GET https://connect.mindcloud.co/v1/universal/cohere/latest/actions/get-embed-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cohere `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cohere/latest/actions/get-embed-job?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cohere/latest/actions/get-embed-job?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
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

Through the native Cohere API, this operation is `GET /v1/embed-jobs/:id` (base URL `https://api.cohere.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-embed-job.md) for the provider-specific parameters and requirements.

