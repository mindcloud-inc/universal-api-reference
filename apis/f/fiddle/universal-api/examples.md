# Fiddle Universal API Examples

These examples use the MindCloud API key and Fiddle connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Inventory Types

Retrieves inventory type records from Fiddle.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fiddle/latest/actions/list-inventory-types?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fiddle/latest/actions/list-inventory-types?${params}`, {
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
      "accountId": "string",
      "accountingCategory": "string",
      "billOfMaterialDefaultMeasurementUnit": {},
      "billOfMaterialDefaultMeasurementUnitId": {},
      "billOfMaterialType": {},
      "changeable": true,
      "createdAt": "string",
      "defaultMeasurementUnit": {
        "abbreviation": "string",
        "description": "string",
        "id": "string",
        "name": "Ava Chen",
        "unitType": "string"
      },
      "defaultMeasurementUnitId": "string",
      "description": "string",
      "hasBillOfMaterial": true,
      "hasFormula": true,
      "id": "string",
      "name": "Ava Chen",
      "prefix": "string",
      "recordType": {},
      "recordTypeId": {},
      "sortIndex": 1,
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Inventory Types action reference](actions/list-inventory-types.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/fiddle/latest/actions/list-inventory-types).

## Create Customer

Creates a new customer in Fiddle.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fiddle/latest/actions/create-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fiddle/latest/actions/create-customer', {
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
      "customer": {
        "createdAt": "2026-05-07T12:00:00.000Z",
        "id": "string",
        "name": "Ava Chen",
        "updatedAt": "2026-05-07T12:00:00.000Z"
      }
    }
  ],
  "meta": {}
}
```

See the full [Create Customer action reference](actions/create-customer.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/fiddle/latest/actions/create-customer).
