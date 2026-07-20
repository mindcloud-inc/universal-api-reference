# Shopify Universal API Examples

These examples use the MindCloud API key and Shopify connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Products

Retrieves products from Shopify with GraphQL.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shopify/latest/actions/list-products?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shopify/latest/actions/list-products?${params}`, {
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
      "createdAt": "string",
      "descriptionHtml": "string",
      "handle": "string",
      "id": "string",
      "images": [
        {
          "altText": "string",
          "src": "string"
        }
      ],
      "metafields": [
        {
          "key": "string",
          "namespace": "Ava Chen",
          "type": "string",
          "value": "string"
        }
      ],
      "nextCursor": "string",
      "options": [
        {
          "name": "Ava Chen",
          "position": 1,
          "values": [
            "string"
          ]
        }
      ],
      "productType": "string",
      "status": "string",
      "tags": [
        "string"
      ],
      "title": "string",
      "updatedAt": "string",
      "variants": [
        {
          "barcode": "string",
          "compareAtPrice": "string",
          "id": "string",
          "inventoryItem": {
            "countryCodeOfOrigin": "string",
            "harmonizedSystemCode": "string",
            "id": "string",
            "unitCost": {
              "amount": "string",
              "currencyCode": "string"
            }
          },
          "inventoryPolicy": "string",
          "inventoryQuantity": 1,
          "metafields": [
            {
              "key": "string",
              "namespace": "Ava Chen",
              "type": "string",
              "value": "string"
            }
          ],
          "price": "string",
          "selectedOptions": [
            {
              "name": "Ava Chen",
              "value": "string"
            }
          ],
          "sku": "string",
          "taxable": true,
          "title": "string"
        }
      ],
      "vendor": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Products action reference](actions/list-products.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/shopify/latest/actions/list-products).

## Activate Inventory Item

Activates an inventory item in Shopify.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/shopify/latest/actions/activate-inventory-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "variables.inventoryItemId": "string",
  "variables.locationId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shopify/latest/actions/activate-inventory-item', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "variables.inventoryItemId": "string",
    "variables.locationId": "string"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [],
  "meta": {}
}
```

See the full [Activate Inventory Item action reference](actions/activate-inventory-item.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/shopify/latest/actions/activate-inventory-item).
