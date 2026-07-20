# Lettermint: Send Multiple Emails in a Batch

Sends multiple emails in a batch through Lettermint.

```
POST https://connect.mindcloud.co/v1/universal/lettermint/latest/actions/send-multiple-emails-in-a-batch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lettermint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/lettermint/latest/actions/send-multiple-emails-in-a-batch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lettermint/latest/actions/send-multiple-emails-in-a-batch', {
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
      "message_id": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message_id` | string | Unique ID of a queued email message in the batch result. |
| `status` | string | Current Lettermint delivery status for the batch item. |

## Native endpoint

Through the native Lettermint API, this operation is `POST /send/batch` (base URL `https://api.lettermint.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-multiple-emails-in-a-batch.md) for the provider-specific parameters and requirements.

