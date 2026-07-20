# BaseLinker: Set Order Product Fields

Updates order product fields in BaseLinker.

```
PUT https://connect.mindcloud.co/v1/universal/baseLinker/latest/actions/set-order-product-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BaseLinker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/baseLinker/latest/actions/set-order-product-fields" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "order_id": 1,
  "order_product_id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/baseLinker/latest/actions/set-order-product-fields', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "order_id": 1,
    "order_product_id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `order_id` | number | yes | Order identifier. |
| `order_product_id` | number | yes | Order product line identifier to update. |
| `name` | string | no | Updated product name. |
| `sku` | string | no | Updated SKU value. |
| `ean` | string | no | Updated EAN value. |
| `price_brutto` | number | no | Updated gross item price. |
| `quantity` | number | no | Updated quantity value. |
| `tax_rate` | number | no | Updated VAT rate percentage. |
| `attributes` | object | no | Updated product attributes payload. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `parameters` | object | no | Optional raw BaseLinker parameters merged with the typed fields before request serialization. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string | SUCCESS when the order item fields were updated. |

## Native endpoint

Through the native BaseLinker API, this operation is `POST /connector.php` (base URL `https://api.baselinker.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-order-product-fields.md) for the provider-specific parameters and requirements.

