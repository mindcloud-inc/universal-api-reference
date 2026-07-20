# Billingo: Get Product Inventory Quantity

Retrieves product quantity from Billingo's default warehouse.

```
GET https://connect.mindcloud.co/v1/universal/billingo/latest/actions/get-product-inventory-quantity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Billingo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/billingo/latest/actions/get-product-inventory-quantity?connectionId=$CONNECTION_ID&id=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "0"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/billingo/latest/actions/get-product-inventory-quantity?${params}`, {
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
| `id` | number | yes | Billingo product ID. Default: `0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "available_quantity": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `available_quantity` | number | Available product quantity in the default warehouse. |

## Native endpoint

Through the native Billingo API, this operation is `GET /inventory/product/:id/quantity` (base URL `https://api.billingo.hu/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-product-inventory-quantity.md) for the provider-specific parameters and requirements.

