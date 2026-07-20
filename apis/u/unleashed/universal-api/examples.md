# Unleashed Universal API Examples

These examples use the MindCloud API key and Unleashed connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Products

Retrieves products from your Unleashed inventory catalog.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/unleashed/latest/actions/list-products?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/unleashed/latest/actions/list-products?${params}`, {
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
      "alternateUnitsOfMeasure": [
        {}
      ],
      "averageLandPrice": 1,
      "copyCommentsForPurchases": true,
      "copyCommentsForSales": true,
      "createdBy": "string",
      "createdOn": "string",
      "defaultPurchasePrice": 1,
      "defaultPurchasesUnitOfMeasure": {},
      "defaultSellPrice": 1,
      "guid": "string",
      "inventoryDetails": [
        {}
      ],
      "isAssembledProduct": true,
      "isBatchTracked": true,
      "isComponent": true,
      "isPurchasable": true,
      "isSellable": true,
      "isSerialized": true,
      "lastCost": 1,
      "lastModifiedOn": "string",
      "maxStockAlertLevel": 1,
      "minStockAlertLevel": 1,
      "neverDiminishing": true,
      "obsolete": true,
      "productCode": "string",
      "productDescription": "string",
      "productGroup": {},
      "supplier": {},
      "taxablePurchase": true,
      "taxableSales": true,
      "unitOfMeasure": {}
    }
  ],
  "meta": {}
}
```

See the full [List Products action reference](actions/list-products.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/unleashed/latest/actions/list-products).

## Create Customer

Creates a new customer in Unleashed.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/unleashed/latest/actions/create-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerCode": "string",
  "customerName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/unleashed/latest/actions/create-customer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerCode": "string",
    "customerName": "Ava Chen"
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
      "addresses": [
        {}
      ],
      "contacts": [
        {}
      ],
      "creditLimit": 1,
      "currency": {},
      "customerCode": "string",
      "customerName": "Ava Chen",
      "customerType": "string",
      "defaultWarehouse": {},
      "discountRate": 1,
      "email": "ava@example.com",
      "guid": "string",
      "hasCreditLimit": true,
      "lastModifiedOn": "string",
      "notes": "string",
      "obsolete": true,
      "paymentTerm": "string",
      "phoneNumber": "string",
      "stopCredit": true,
      "taxable": true,
      "taxCode": "string",
      "taxRate": 1,
      "website": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Customer action reference](actions/create-customer.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/unleashed/latest/actions/create-customer).
