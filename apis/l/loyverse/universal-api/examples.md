# Loyverse Universal API Examples

These examples use the MindCloud API key and Loyverse connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Items

Retrieves item records from the Loyverse catalog.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/loyverse/latest/actions/list-items?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/loyverse/latest/actions/list-items?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "cursor": "string",
      "items": [
        {
          "categoryId": "string",
          "color": "string",
          "components": [
            {
              "quantity": 1,
              "variantId": "string"
            }
          ],
          "createdAt": "2026-05-07T12:00:00.000Z",
          "deletedAt": "2026-05-07T12:00:00.000Z",
          "description": "string",
          "form": "string",
          "handle": "string",
          "id": "string",
          "imageUrl": "https://example.com",
          "isComposite": true,
          "itemName": "Ava Chen",
          "modifiersIds": [
            "string"
          ],
          "option1Name": "Ava Chen",
          "option2Name": "Ava Chen",
          "option3Name": "Ava Chen",
          "primarySupplierId": "string",
          "referenceId": "string",
          "soldByWeight": true,
          "taxIds": [
            "string"
          ],
          "trackStock": true,
          "updatedAt": "2026-05-07T12:00:00.000Z",
          "useProduction": true,
          "variants": [
            {
              "barcode": "string",
              "cost": 1,
              "createdAt": "2026-05-07T12:00:00.000Z",
              "defaultPrice": 1,
              "defaultPricingType": "string",
              "deletedAt": "2026-05-07T12:00:00.000Z",
              "itemId": "string",
              "option1Value": "string",
              "option2Value": "string",
              "option3Value": "string",
              "purchaseCost": 1,
              "referenceVariantId": "string",
              "sku": "string",
              "stores": [
                {
                  "availableForSale": true,
                  "lowStock": 1,
                  "optimalStock": 1,
                  "price": 1,
                  "pricingType": "string",
                  "storeId": "string"
                }
              ],
              "updatedAt": "2026-05-07T12:00:00.000Z",
              "variantId": "string"
            }
          ]
        }
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Items action reference](actions/list-items.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/loyverse/latest/actions/list-items).

## Batch Update Inventory Levels

Updates inventory levels in batch in Loyverse.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/loyverse/latest/actions/batch-update-inventory-levels" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/loyverse/latest/actions/batch-update-inventory-levels', {
  method: 'PUT',
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

Example response:

```json
{
  "success": true,
  "data": [
    {
      "inventoryLevels": [
        {
          "inStock": 1,
          "storeId": "string",
          "updatedAt": "2026-05-07T12:00:00.000Z",
          "variantId": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

See the full [Batch Update Inventory Levels action reference](actions/batch-update-inventory-levels.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/loyverse/latest/actions/batch-update-inventory-levels).
