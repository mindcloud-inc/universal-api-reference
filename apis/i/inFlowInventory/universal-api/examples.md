# inFlow Inventory Universal API Examples

These examples use the MindCloud API key and inFlow Inventory connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Products

Retrieves product records from inFlow Inventory.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/inFlowInventory/latest/actions/list-products?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/inFlowInventory/latest/actions/list-products?${params}`, {
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
      "autoAssemble": true,
      "categoryId": "string",
      "description": "string",
      "height": "string",
      "isActive": true,
      "isManufacturable": true,
      "itemType": "string",
      "lastModifiedById": "string",
      "lastModifiedDateTime": "2026-05-07T12:00:00.000Z",
      "lastVendorId": "string",
      "length": "string",
      "name": "Ava Chen",
      "productId": "string",
      "purchasingUom": {
        "name": "Ava Chen"
      },
      "salesUom": {
        "name": "Ava Chen"
      },
      "sku": "string",
      "standardUomName": "Ava Chen",
      "timestamp": "string",
      "trackExpiry": true,
      "trackLots": true,
      "trackSerials": true,
      "weight": "string",
      "width": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Products action reference](actions/list-products.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/inFlowInventory/latest/actions/list-products).

## Insert or Update Customer

Inserts or updates a customer in inFlow Inventory.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/inFlowInventory/latest/actions/insert-or-update-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/inFlowInventory/latest/actions/insert-or-update-customer', {
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
      "contactName": "Ava Chen",
      "customerId": "string",
      "defaultBillingAddressId": "string",
      "defaultLocationId": "string",
      "defaultPaymentMethod": "string",
      "defaultPaymentTermsId": "string",
      "defaultSalesRep": "string",
      "defaultSalesRepTeamMemberId": "string",
      "defaultShippingAddressId": "string",
      "discount": "string",
      "email": "ava@example.com",
      "fax": "string",
      "isActive": true,
      "lastModifiedById": "string",
      "lastModifiedDttm": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "phone": "string",
      "pricingSchemeId": "string",
      "remarks": "string",
      "taxExemptNumber": "string",
      "taxingSchemeId": "string",
      "timestamp": "string",
      "website": "string"
    }
  ],
  "meta": {}
}
```

See the full [Insert or Update Customer action reference](actions/insert-or-update-customer.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/inFlowInventory/latest/actions/insert-or-update-customer).
