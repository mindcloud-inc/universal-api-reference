# Shopify: List Order Payment Transactions



```
GET https://connect.mindcloud.co/v1/universal/shopify/latest/actions/get-order-transactions-graph-ql
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shopify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shopify/latest/actions/get-order-transactions-graph-ql?connectionId=$CONNECTION_ID&variables.orderId=gid%3A%2F%2Fshopify%2FOrder%2F1234567890" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "variables.orderId": "gid://shopify/Order/1234567890"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shopify/latest/actions/get-order-transactions-graph-ql?${params}`, {
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
| `variables` | object | no | Order selection inputs. |
| `variables.orderId` | string | yes | The Shopify GraphQL Order ID to retrieve payment transactions for. Example: `gid://shopify/Order/1234567890`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Shopify API returns.

## Native endpoint

Through the native Shopify API, this operation is `POST 2026-07/graphql.json` (base URL `https://{{credentials.storeName}}.myshopify.com/admin/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-order-transactions-graph-ql.md) for the provider-specific parameters and requirements.

