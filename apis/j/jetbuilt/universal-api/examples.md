# Jetbuilt Universal API Examples

These examples use the MindCloud API key and Jetbuilt connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Project Items



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jetbuilt/latest/actions/get-project-items?connectionId=$CONNECTION_ID&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jetbuilt/latest/actions/get-project-items?${params}`, {
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
      "bundle": {},
      "cost": "string",
      "createdAt": "string",
      "currencyIso": "string",
      "custom": true,
      "custom?": true,
      "customProductId": {},
      "discount": "string",
      "engineeringReleased": true,
      "externalNotes": "string",
      "hidden": true,
      "id": 1,
      "kind": "string",
      "laborPreset": {},
      "manufacturerId": 1,
      "manufacturerName": "Ava Chen",
      "mapp": {},
      "model": "string",
      "msrp": {},
      "msrpDiscountPercent": {},
      "notes": {},
      "option": {},
      "ownerFurnished": true,
      "partNumber": {},
      "phase": {},
      "price": "string",
      "productId": 1,
      "purchasingReleased": true,
      "purchasingSource": {},
      "quantity": "string",
      "quantityPerBundle": {},
      "quantityPerRoom": "string",
      "room": {
        "id": 1,
        "name": "Ava Chen",
        "quantity": 1
      },
      "selectedPurchasingVendor": {},
      "shippingPrice": "string",
      "shortDescription": "string",
      "subcontractLaborCost": "string",
      "subcontractLaborPrice": "string",
      "subtotalEquipmentPrice": "string",
      "system": {
        "id": 1,
        "name": "Ava Chen"
      },
      "tag": {},
      "taxEquipment": true,
      "taxShipping": true,
      "totalEquipmentPrice": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Project Items action reference](actions/get-project-items.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/jetbuilt/latest/actions/get-project-items).

## Create a Product



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/jetbuilt/latest/actions/create-a-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "productDatabaseId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/jetbuilt/latest/actions/create-a-product', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "productDatabaseId": "string"
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

See the full [Create a Product action reference](actions/create-a-product.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/jetbuilt/latest/actions/create-a-product).
