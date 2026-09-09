# Walmart: Update Inventory

Replace the stock level for one SKU.

```
PUT https://connect.mindcloud.co/v1/universal/walmart/latest/actions/update-inventory
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Walmart `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/walmart/latest/actions/update-inventory" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "bodySku": "string",
  "sku": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/walmart/latest/actions/update-inventory', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "bodySku": "string",
    "sku": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `bodySku` | string | yes |  |
| `quantity.unit` | string | no | A unit of measure. Walmart Marketplace supports only EACH which indicates one individual sellable item. Default: `EACH`. |
| `sku` | string | yes | A unique alphanumeric ID you assign to each item. Use the same value in every request that references the item, including your XSD catalog file. |
| `quantity` | object | no | The quantity that customers have ordered but you haven't shipped yet. |
| `quantity.amount` | number | no | The number of units pending shipment. |
| `inventoryAvailableDate` | string | no | The date when this inventory becomes available at the ship node. Use ISO 8601 format (YYYY-MM-DD). If you omit this field, Walmart treats the inventory as available today. |
| `shipNode` | list<string> | no | The unique ID of the ship node (fulfillment center) where you want to update inventory. If you omit this parameter, Walmart updates inventory at your default ship node. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `isDynamicSandbox` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "inventoryAvailableDate": "string",
      "quantity": {
        "amount": 1,
        "unit": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `inventoryAvailableDate` | string |  |
| `quantity.amount` | number |  |
| `quantity.unit` | string |  |

## Native endpoint

Through the native Walmart API, this operation is `PUT /v3/inventory` (base URL `https://{{credentials.environment}}.walmartapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-inventory.md) for the provider-specific parameters and requirements.

