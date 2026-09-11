# BigCommerce: Get Webhooks



```
GET https://connect.mindcloud.co/v1/universal/bigcommerce/latest/actions/get-webhooks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BigCommerce `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bigcommerce/latest/actions/get-webhooks?connectionId=$CONNECTION_ID&scope=string&destination=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "scope": "string",
  "destination": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bigcommerce/latest/actions/get-webhooks?${params}`, {
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
| `scope` | string | yes |  |
| `destination` | string | yes | URL must be active, return a 200 response, and be served on port 443. Custom ports arenʼt currently supported. |
| `isActive` | boolean | no | Boolean value that indicates whether the webhook is active or not. A webhook subscription becomes deactivated after 90 days of inactivity. |
| `headers` | object | no | Headers used to validate that webhooks are active. You can pass in any number of custom headers to validate webhooks are being returned. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native BigCommerce API returns.

## Native endpoint

Through the native BigCommerce API, this operation is `GET /v3/hooks` (base URL `https://api.bigcommerce.com/stores/{{credentials.storeHash}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-webhooks.md) for the provider-specific parameters and requirements.

