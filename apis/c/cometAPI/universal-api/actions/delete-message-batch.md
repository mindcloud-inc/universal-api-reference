# CometAPI: Delete Message Batch



```
DELETE https://connect.mindcloud.co/v1/universal/cometAPI/latest/actions/delete-message-batch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CometAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/cometAPI/latest/actions/delete-message-batch?connectionId=$CONNECTION_ID&messageBatchId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "messageBatchId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cometAPI/latest/actions/delete-message-batch?${params}`, {
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
| `messageBatchId` | string | yes | Message batch ID to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deleted": true,
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deleted` | boolean |  |
| `id` | string |  |

## Native endpoint

Through the native CometAPI API, this operation is `DELETE /v1/messages/batches/:message_batch_id` (base URL `https://api.cometapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-message-batch.md) for the provider-specific parameters and requirements.

