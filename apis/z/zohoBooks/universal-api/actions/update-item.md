# Zoho Books: Update Item



```
PUT https://connect.mindcloud.co/v1/universal/zohoBooks/latest/actions/update-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Books `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zohoBooks/latest/actions/update-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "itemId": "string",
  "organizationId": "string",
  "name": "Codex Stage3 Item 20260311 Updated",
  "rate": "150"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoBooks/latest/actions/update-item', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "itemId": "string",
    "organizationId": "string",
    "name": "Codex Stage3 Item 20260311 Updated",
    "rate": "150"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `itemId` | list | yes |  |
| `organizationId` | list | yes |  |
| `name` | string | yes | Example: `Codex Stage3 Item 20260311 Updated`. |
| `rate` | number | yes | Example: `150`. |
| `description` | string | no | Example: `Updated during Zoho Books Stage 3 validation`. |
| `sku` | string | no | Example: `CODEX-STAGE3-ITEM-20260311`. |
| `productType` | list | no | One of: `0`, `1`, `2`, `3`, `4`. |
| `itemType` | list | no | One of: `0`, `1`, `2`, `3`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `taxId` | string | no | Example: `1234567890`. |
| `isTaxable` | boolean | no |  |
| `taxExemptionId` | string | no | Example: `1234567890`. |
| `accountId` | string | no | Example: `1234567890`. |
| `purchaseDescription` | string | no | Example: `Warehouse replenishment`. |
| `purchaseRate` | number | no | Example: `80`. |
| `purchaseAccountId` | string | no | Example: `1234567890`. |
| `inventoryAccountId` | string | no | Example: `1234567890`. |
| `vendorId` | string | no | Example: `1234567890`. |
| `reorderLevel` | number | no | Example: `10`. |
| `locations[]` | array<object> | no |  |
| `locations[].locationId` | string | no | Example: `1234567890`. |
| `locations[].initialStock` | number | no | Example: `25`. |
| `locations[].initialStockRate` | number | no | Example: `80`. |

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

Through the native Zoho Books API, this operation is `PUT /items/:item_id` (base URL `https://www.zohoapis.com/books/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-item.md) for the provider-specific parameters and requirements.

