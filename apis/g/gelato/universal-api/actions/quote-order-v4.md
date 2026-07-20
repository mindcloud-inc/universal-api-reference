# Gelato: Quote Order v4

Retrieves shipping quotes for order items in Gelato v4.

```
GET https://connect.mindcloud.co/v1/universal/gelato/latest/actions/quote-order-v4
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gelato `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gelato/latest/actions/quote-order-v4?connectionId=$CONNECTION_ID&orderReferenceId=string&customerReferenceId=string&currency=string&recipient=%5Bobject%20Object%5D&products%5B%5D=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "orderReferenceId": "string",
  "customerReferenceId": "string",
  "currency": "string",
  "recipient": "[object Object]",
  "products[]": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gelato/latest/actions/quote-order-v4?${params}`, {
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
| `orderReferenceId` | string | yes |  |
| `customerReferenceId` | string | yes |  |
| `currency` | string | yes |  |
| `recipient` | object | yes |  |
| `products[]` | array<object> | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Gelato API returns.

## Native endpoint

Through the native Gelato API, this operation is `POST /v4/orders:quote` (base URL `https://order.gelatoapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/quote-order-v4.md) for the provider-specific parameters and requirements.

