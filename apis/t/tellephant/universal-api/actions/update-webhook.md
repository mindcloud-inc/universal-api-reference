# Tellephant: Update webhook

Updates a webhook configuration in Tellephant.

```
PUT https://connect.mindcloud.co/v1/universal/tellephant/latest/actions/update-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tellephant `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/tellephant/latest/actions/update-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "webhookType": "delivery_response",
  "webhookEndpoint": "string",
  "webhookStatus": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tellephant/latest/actions/update-webhook', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "webhookType": "delivery_response",
    "webhookEndpoint": "string",
    "webhookStatus": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `webhookType` | list | yes | Webhook type to update: delivery_response or incoming_message. One of: `delivery_response`, `incoming_message`. |
| `webhookEndpoint` | string | yes | Webhook destination URL. |
| `webhookStatus` | boolean | yes | Whether the webhook is enabled. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "error": {},
      "message": "string",
      "status": true,
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `error` | object |  |
| `message` | string |  |
| `status` | boolean |  |
| `success` | boolean |  |

## Native endpoint

Through the native Tellephant API, this operation is `POST https://app.tellephant.com/api/v2/user/webhook/update` (base URL `https://api.tellephant.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-webhook.md) for the provider-specific parameters and requirements.

