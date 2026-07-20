# Cohere: Get Batch

Retrieves a batch from Cohere.

```
GET https://connect.mindcloud.co/v1/universal/cohere/latest/actions/get-batch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cohere `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cohere/latest/actions/get-batch?connectionId=$CONNECTION_ID&id=batch_id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "batch_id"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cohere/latest/actions/get-batch?${params}`, {
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
| `id` | string | yes | The Cohere batch ID to retrieve. Default: `batch_id`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "batch": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `batch` | object |  |

## Native endpoint

Through the native Cohere API, this operation is `GET /v2/batches/:id` (base URL `https://api.cohere.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-batch.md) for the provider-specific parameters and requirements.

