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
  "connectionId": "$CONNECTION_ID",
  "referenceId": "string",
  "name": "Ava Chen"
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
    connectionId,
    "referenceId": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `referenceId` | string | yes |  |
| `sku` | string | no |  |
| `name` | string | yes |  |
| `barcode` | string | no |  |
| `gtin` | string | no | Global Trade Item Number - unique and internationally recognized identifier assigned to item by company GS1. |
| `upc` | string | no | Universal Product Code - Unique external identifier |
| `unit_price` | number | no | The price of one unit |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ShipBob API returns.

## Native endpoint

Through the native ShipBob API, this operation is `POST 1.0/product` (base URL `https://{{credentials.apiSubdomain}}.shipbob.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/post-product.md) for the provider-specific parameters and requirements.

