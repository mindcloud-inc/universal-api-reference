# Hyperstack Certificates: Subscribe to Webhook



```
POST https://connect.mindcloud.co/v1/universal/hyperstack/latest/actions/subscribe-to-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hyperstack Certificates `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hyperstack/latest/actions/subscribe-to-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "events": {},
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hyperstack/latest/actions/subscribe-to-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "events": {},
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `events` | object<string> | yes | Array of event names to subscribe to. Currently supported: credential.issued. |
| `url` | string | yes | The webhook URL to receive events. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Confirmation message returned by Hyperstack. |
| `success` | boolean | Indicates whether the webhook subscription was created or updated. |

## Native endpoint

Through the native Hyperstack Certificates API, this operation is `POST /webhook/subscribe` (base URL `https://api.thehyperstack.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/subscribe-to-webhook.md) for the provider-specific parameters and requirements.

