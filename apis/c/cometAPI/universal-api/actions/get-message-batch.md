# CometAPI: Get Message Batch



```
GET https://connect.mindcloud.co/v1/universal/cometAPI/latest/actions/get-message-batch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CometAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cometAPI/latest/actions/get-message-batch?connectionId=$CONNECTION_ID&messageBatchId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "messageBatchId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cometAPI/latest/actions/get-message-batch?${params}`, {
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
| `messageBatchId` | string | yes | Message batch ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "processing_status": "string",
      "request_counts": {},
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `processing_status` | string |  |
| `request_counts` | object |  |
| `type` | string |  |

## Native endpoint

Through the native CometAPI API, this operation is `GET /v1/messages/batches/:message_batch_id` (base URL `https://api.cometapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-message-batch.md) for the provider-specific parameters and requirements.

