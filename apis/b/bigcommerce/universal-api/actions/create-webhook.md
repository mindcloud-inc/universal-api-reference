# BigCommerce: Create Webhook



```
POST https://connect.mindcloud.co/v1/universal/bigcommerce/latest/actions/create-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BigCommerce `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bigcommerce/latest/actions/create-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "scope": "string",
  "destination": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bigcommerce/latest/actions/create-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "scope": "string",
    "destination": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `scope` | string | yes |  |
| `destination` | string | yes | URL must be active, return a 200 response, and be served on port 443. Custom ports arenʼt currently supported. |
| `isActive` | boolean | no | Boolean value that indicates whether the webhook is active or not. A webhook subscription becomes deactivated after 90 days of inactivity. |
| `headers` | object | no | Headers used to validate that webhooks are active. You can pass in any number of custom headers to validate webhooks are being returned. |
| `eventsHistoryEnabled` | boolean | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native BigCommerce API returns.

## Native endpoint

Through the native BigCommerce API, this operation is `POST /v3/hooks` (base URL `https://api.bigcommerce.com/stores/{{credentials.storeHash}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook.md) for the provider-specific parameters and requirements.

