# Shopify: Set Fixed Price on Price List



```
PUT https://connect.mindcloud.co/v1/universal/shopify/latest/actions/set-fixed-price-on-price-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shopify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/shopify/latest/actions/set-fixed-price-on-price-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "priceListId": "Select a Shopify price list",
  "variantId": "gid://shopify/ProductVariant/43729076",
  "amount": "100.00",
  "currencyCode": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shopify/latest/actions/set-fixed-price-on-price-list', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "priceListId": "Select a Shopify price list",
    "variantId": "gid://shopify/ProductVariant/43729076",
    "amount": "100.00",
    "currencyCode": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `priceListId` | list | yes | Select the Shopify price list that should receive the fixed variant price. Example: `Select a Shopify price list`. |
| `variantId` | string | yes | Shopify ProductVariant GID whose catalog price will be set. Example: `gid://shopify/ProductVariant/43729076`. |
| `amount` | number | yes | Absolute fixed price amount for the variant. Example: `100.00`. |
| `currencyCode` | list<string> | yes | Currency code matching the price list currency. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Shopify API returns.

## Native endpoint

Through the native Shopify API, this operation is `POST 2026-07/graphql.json` (base URL `https://{{credentials.storeName}}.myshopify.com/admin/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-fixed-price-on-price-list.md) for the provider-specific parameters and requirements.

