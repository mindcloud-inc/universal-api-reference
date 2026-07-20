# SigParser: Create Webhook



```
POST https://connect.mindcloud.co/v1/universal/sigParser/latest/actions/create-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SigParser `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sigParser/latest/actions/create-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com",
  "action": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sigParser/latest/actions/create-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com",
    "action": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes | The webhook URL to post events to. |
| `action` | string | yes | Webhook event type, such as contact.createorupdate or company.createorupdate. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `batchFrequencyCronExpression` | string | no | Cron frequency for batching webhook delivery. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native SigParser API returns.

## Native endpoint

Through the native SigParser API, this operation is `POST /api/Webhooks` (base URL `https://ipaas.sigparser.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook.md) for the provider-specific parameters and requirements.

