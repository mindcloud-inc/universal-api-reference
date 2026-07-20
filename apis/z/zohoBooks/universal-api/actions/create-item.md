# Zoho Books: Create Item



```
POST https://connect.mindcloud.co/v1/universal/zohoBooks/latest/actions/create-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Books `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoBooks/latest/actions/create-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "organizationId": "string",
  "name": "Hard Drive",
  "rate": "120"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoBooks/latest/actions/create-item', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "organizationId": "string",
    "name": "Hard Drive",
    "rate": "120"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `organizationId` | list<string> | yes | ID of the organization. |
| `name` | string | yes | Name of the item. Example: `Hard Drive`. |
| `rate` | number | yes | Price of the item. Example: `120`. |
| `description` | string | no | Description for the item. Example: `500GB external SSD`. |
| `sku` | string | no | SKU value for the item. Example: `HD-500GB`. |
| `productType` | list<string> | no | Type of the item. One of: `capital_goods`, `capital_service`, `digital_service`, `goods`, `service`. |
| `itemType` | list<string> | no | Commercial type of the item. One of: `inventory`, `purchases`, `sales`, `sales_and_purchases`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `taxId` | string | no | Tax ID for the item. Example: `1234567890`. |
| `isTaxable` | boolean | no | Whether the item is taxable. |
| `taxExemptionId` | string | no | Tax exemption ID when the item is not taxable. Example: `1234567890`. |
| `accountId` | string | no | Revenue account ID for the item. Example: `1234567890`. |
| `vendorId` | string | no | Preferred vendor ID. Example: `1234567890`. |
| `reorderLevel` | number | no | Reorder level for the item. Example: `10`. |
| `purchaseDescription` | string | no | Purchase description for the item. Example: `Warehouse replenishment`. |
| `purchaseRate` | number | no | Purchase price of the item. Example: `80`. |
| `purchaseAccountId` | string | no | COGS account ID for purchase or inventory items. Example: `1234567890`. |
| `inventoryAccountId` | string | no | Inventory account ID for inventory items. Example: `1234567890`. |
| `locations[]` | array<object> | no | Per-location opening stock details. |
| `locations[].locationId` | string | no | Location ID. Example: `1234567890`. |
| `locations[].initialStock` | number | no | Opening stock for the location. Example: `25`. |
| `locations[].initialStockRate` | number | no | Unit price of the opening stock. Example: `80`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": "string",
      "accountName": "Ava Chen",
      "createdTime": "string",
      "description": "string",
      "hasAttachment": true,
      "isTaxable": true,
      "itemId": "string",
      "itemType": "string",
      "lastModifiedTime": "string",
      "name": "Ava Chen",
      "productTaxCategory": {},
      "productType": "string",
      "purchaseRate": 1,
      "rate": 1,
      "sku": "string",
      "status": "string",
      "tags": [
        {}
      ],
      "unit": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | string | Associated sales account ID. |
| `accountName` | string | Associated sales account name. |
| `createdTime` | string | Creation timestamp. |
| `description` | string | Item description. |
| `hasAttachment` | boolean | Whether the item has an attachment. |
| `isTaxable` | boolean | Whether the item is taxable. |
| `itemId` | string | Unique identifier of the item. |
| `itemType` | string | Type of the item. |
| `lastModifiedTime` | string | Last modification timestamp. |
| `name` | string | Item name. |
| `productTaxCategory` | object | Product tax category details. |
| `productType` | string | Product classification of the item. |
| `purchaseRate` | number | Purchase rate of the item. |
| `rate` | number | Sales rate of the item. |
| `sku` | string | Stock keeping unit. |
| `status` | string | Item status. |
| `tags` | array<object> | Tags associated with the item. |
| `unit` | string | Measurement unit for the item. |

## Native endpoint

Through the native Zoho Books API, this operation is `POST /items` (base URL `https://www.zohoapis.com/books/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-item.md) for the provider-specific parameters and requirements.

