# Printify: Create Webhook

Creates a webhook in Printify.

```
POST https://connect.mindcloud.co/v1/universal/printify/latest/actions/create-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Printify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/printify/latest/actions/create-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "shop_id": "27141936",
  "topic": "order:created",
  "url": "https://example.com/webhooks/order/created"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/printify/latest/actions/create-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "shop_id": "27141936",
    "topic": "order:created",
    "url": "https://example.com/webhooks/order/created"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `shop_id` | number | yes | Printify shop id. Default: `27141936`. |
| `topic` | string | yes | Webhook event topic. Default: `order:created`. |
| `url` | string | yes | Destination URL for webhook delivery. Default: `https://example.com/webhooks/order/created`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "shopId": "string",
      "topic": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `shopId` | string |  |
| `topic` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Printify API, this operation is `POST /shops/:shop_id/webhooks.json` (base URL `https://api.printify.com/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook.md) for the provider-specific parameters and requirements.

