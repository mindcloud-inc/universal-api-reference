# Katana Universal API Examples

These examples use the MindCloud API key and Katana connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Retrieve Current Factory

Retrieves the current factory from Katana.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/katana/latest/actions/retrieve-current-factory?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/katana/latest/actions/retrieve-current-factory?${params}`, {
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
      "baseCurrencyCode": "string",
      "defaultManufacturingLocationId": 1,
      "defaultPoLeadTime": "string",
      "defaultPurchasesLocationId": 1,
      "defaultSalesLocationId": 1,
      "defaultSoDeliveryTime": "string",
      "displayName": "Ava Chen",
      "inventoryClosingDate": "string",
      "legalAddress": {
        "city": "string",
        "country": "string",
        "line1": "string",
        "line2": "string",
        "state": "string",
        "zip": "string"
      },
      "legalName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Retrieve Current Factory action reference](actions/retrieve-current-factory.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/katana/latest/actions/retrieve-current-factory).

## Create Customer

Creates a new customer in Katana.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/katana/latest/actions/create-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/katana/latest/actions/create-customer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
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
        {
          "city": "string",
          "company": "string",
          "country": "string",
          "createdAt": "string",
          "customerId": 1,
          "entityType": "string",
          "firstName": "Ava",
          "id": 1,
          "lastName": "Chen",
          "line1": "string",
          "line2": "string",
          "phone": "string",
          "state": "string",
          "updatedAt": "string",
          "zip": "string"
        }
      ],
      "category": "string",
      "comment": "string",
      "company": "string",
      "createdAt": "string",
      "currency": "string",
      "defaultBillingId": 1,
      "defaultShippingId": 1,
      "deletedAt": "string",
      "discountRate": 1,
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": 1,
      "lastName": "Chen",
      "name": "Ava Chen",
      "phone": "string",
      "referenceId": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Customer action reference](actions/create-customer.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/katana/latest/actions/create-customer).
