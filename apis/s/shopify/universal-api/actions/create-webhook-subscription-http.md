# Shopify: Create Webhook Subscription (HTTP)

Creates an HTTP webhook subscription in Shopify.

```
POST https://connect.mindcloud.co/v1/universal/shopify/latest/actions/create-webhook-subscription-http
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shopify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/shopify/latest/actions/create-webhook-subscription-http" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "variables.webhookSubscription.callbackUrl": "https://example.com",
  "variables.topic": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shopify/latest/actions/create-webhook-subscription-http', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "variables.webhookSubscription.callbackUrl": "https://example.com",
    "variables.topic": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `query` | string | no |  |
| `variables.webhookSubscription.callbackUrl` | string | yes | URL where the webhook subscription should send the POST request when the event occurs. |
| `variables` | object | no |  |
| `variables.topic` | string | yes |  |
| `variables.webhookSubscription.filter` | string | no |  |
| `variables.webhookSubscription.metafieldNamespaces` | string | no | Accepts multiple values as an array. Default: `custom`. |
| `variables.webhookSubscription` | object | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Shopify API returns.

## Native endpoint

Through the native Shopify API, this operation is `POST 2024-10/graphql.json` (base URL `https://{{credentials.storeName}}.myshopify.com/admin/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook-subscription-http.md) for the provider-specific parameters and requirements.

