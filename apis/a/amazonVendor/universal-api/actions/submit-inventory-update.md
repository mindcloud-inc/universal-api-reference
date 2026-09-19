# Amazon Vendor: Submit Inventory Update



```
PUT https://connect.mindcloud.co/v1/universal/amazonVendor/latest/actions/submit-inventory-update
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Amazon Vendor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/amazonVendor/latest/actions/submit-inventory-update" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "inventory.sellingParty.partyId": "string",
  "warehouseId": "string",
  "inventory.isFullUpdate": "False",
  "inventory.items[]": [
    "string"
  ],
  "inventory.sellingParty": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/amazonVendor/latest/actions/submit-inventory-update', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "inventory.sellingParty.partyId": "string",
    "warehouseId": "string",
    "inventory.isFullUpdate": "False",
    "inventory.items[]": ["string"],
    "inventory.sellingParty": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `inventory.items[].buyerProductIdentifier` | string | no | The buyer-selected product identifier for the item. Submit either this value or the vendor product identifier. |
| `inventory.sellingParty.partyId` | string | yes | Assigned identification for the party. |
| `warehouseId` | string | yes | Identifier for the warehouse for which to update inventory. |
| `inventory` | object | no | Inventory details required to update some or all items for the requested warehouse. |
| `inventory.items[].vendorProductIdentifier` | string | no | The vendor-selected product identifier for the item. Submit either this value or the buyer product identifier. Example: `7Q89K11`. |
| `inventory.isFullUpdate` | boolean | yes | When true, this request contains a full feed; otherwise it contains a partial feed. A full feed must include all warehouse items, and omitted items become unavailable. A partial feed should include only items whose inventory must change; other items remain unchanged. Default: `False`. |
| `inventory.items[]` | array | yes |  |
| `inventory.items[].availableQuantity` | object | no | Total item quantity available in the warehouse. |
| `inventory.sellingParty` | object | yes |  |
| `inventory.items[].availableQuantity.amount` | number | no | Quantity of units available for a specific item. Example: `10`. |
| `inventory.items[].availableQuantity.unitOfMeasure` | string | no | Unit of measure for the available quantity. Default: `Each`. Example: `Each`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `inventory.items[].isObsolete` | boolean | no | When true, the item is permanently unavailable. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Amazon Vendor API returns.

## Native endpoint

Through the native Amazon Vendor API, this operation is `POST /vendor/directFulfillment/inventory/v1/warehouses/:warehouseId/items` (base URL `https://sellingpartnerapi-{{credentials.region}}.amazon.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/submit-inventory-update.md) for the provider-specific parameters and requirements.

