# xAI: Get Batch

Retrieves a batch from the xAI API.

```
GET https://connect.mindcloud.co/v1/universal/xAI/latest/actions/get-batch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xAI/latest/actions/get-batch?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xAI/latest/actions/get-batch?${params}`, {
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
| `batch_id` | string | no | Unique batch identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "batch_id": "string",
      "create_time": "string",
      "name": "Ava Chen",
      "state": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `batch_id` | string |  |
| `create_time` | string |  |
| `name` | string |  |
| `state` | object |  |

## Native endpoint

Through the native xAI API, this operation is `GET /batches/:batch_id` (base URL `https://api.x.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-batch.md) for the provider-specific parameters and requirements.

