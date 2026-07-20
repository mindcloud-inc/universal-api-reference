# Anthropic: Delete Message Batch

Deletes a message batch from Anthropic.

```
DELETE https://connect.mindcloud.co/v1/universal/anthropic/latest/actions/delete-message-batch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Anthropic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/anthropic/latest/actions/delete-message-batch?connectionId=$CONNECTION_ID&messageBatchId=msgbatch_123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "messageBatchId": "msgbatch_123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/anthropic/latest/actions/delete-message-batch?${params}`, {
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
| `messageBatchId` | string | yes | The Message Batch ID. Example: `msgbatch_123`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
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
| `type` | string |  |

## Native endpoint

Through the native Anthropic API, this operation is `DELETE /v1/messages/batches/:message_batch_id` (base URL `https://api.anthropic.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-message-batch.md) for the provider-specific parameters and requirements.

