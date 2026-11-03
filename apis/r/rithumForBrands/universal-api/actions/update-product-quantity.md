# Rithum for Brands: Update Product Quantity

Update Product Quantity at one or more Distribution Centers.

```
PUT https://connect.mindcloud.co/v1/universal/rithumForBrands/latest/actions/update-product-quantity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rithum for Brands `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rithumForBrands/latest/actions/update-product-quantity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "productID": "string",
  "updateType": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rithumForBrands/latest/actions/update-product-quantity', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "productID": "string",
    "updateType": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `productID` | string | yes | The Rithum-defined unique ID (not the Sku value) of the product you want to update quantities for. |
| `updates[].distributionCenterID` | number | no | Rithum's Distribution Center Unique ID. |
| `updates[].quantity` | number | no | Available Quantity for the product at the Distribution Center ID provided. |
| `updateType` | list<string> | yes | This value determines how the platform will interpret the quantity. |
| `updates[]` | array | no | A list of Qtys for this product at each Distribution Center. *Note: 'Quantity' and 'Distribution Center ID' are required arguments* |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Rithum for Brands API returns.

## Native endpoint

Through the native Rithum for Brands API, this operation is `POST Products(:productID)/UpdateQuantity` (base URL `https://api.channeladvisor.com/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-product-quantity.md) for the provider-specific parameters and requirements.

