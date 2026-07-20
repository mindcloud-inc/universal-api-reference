# Anthropic: Retrieve Message Batch Results

Retrieves results for an Anthropic message batch.

```
GET https://connect.mindcloud.co/v1/universal/anthropic/latest/actions/retrieve-message-batch-results
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Anthropic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/anthropic/latest/actions/retrieve-message-batch-results?connectionId=$CONNECTION_ID&messageBatchId=msgbatch_123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "messageBatchId": "msgbatch_123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/anthropic/latest/actions/retrieve-message-batch-results?${params}`, {
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
      "customId": "string",
      "result": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customId` | string |  |
| `result` | object |  |

## Native endpoint

Through the native Anthropic API, this operation is `GET /v1/messages/batches/:message_batch_id/results` (base URL `https://api.anthropic.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-message-batch-results.md) for the provider-specific parameters and requirements.

