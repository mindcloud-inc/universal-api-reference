# ShipBob: Post Product



```
POST https://connect.mindcloud.co/v1/universal/shipbob/latest/actions/post-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ShipBob `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/shipbob/latest/actions/post-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shipbob/latest/actions/post-product', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `is_quarantine` | string | no |  |
| `variants.sku` | string | no |  |
| `name` | string | no |  |
| `variants.upc` | string | no |  |
| `taxonomy_id` | number | no |  |
| `type_id` | number | no | The product type ID (1 = Regular, 2 = Bundle) |
| `variants` | object | no | Example: `List of variants to create with the product. At least one variant is required. Each variant must have a unique SKU.`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ShipBob API returns.

## Native endpoint

Through the native ShipBob API, this operation is `POST 2026-07/product` (base URL `https://{{credentials.apiSubdomain}}.shipbob.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/post-product.md) for the provider-specific parameters and requirements.

