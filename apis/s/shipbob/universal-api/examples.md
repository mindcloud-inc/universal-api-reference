# ShipBob Universal API Examples

These examples use the MindCloud API key and ShipBob connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Inventory Levels by Location



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shipbob/latest/actions/list-inventory-levels-by-location?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shipbob/latest/actions/list-inventory-levels-by-location?${params}`, {
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
      "inventoryId": 1,
      "locations": [
        {
          "awaitingQuantity": 1,
          "committedQuantity": 1,
          "damagedQuantity": 1,
          "fulfillableQuantity": 1,
          "internalTransferQuantity": 1,
          "locationId": 1,
          "name": "Ava Chen",
          "onHandQuantity": 1,
          "quarantineQuantity": 1
        }
      ],
      "name": "Ava Chen",
      "sku": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Inventory Levels by Location action reference](actions/list-inventory-levels-by-location.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/shipbob/latest/actions/list-inventory-levels-by-location).

## Create Return Order



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/shipbob/latest/actions/create-return-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fulfillmentCenter": {},
  "fulfillmentCenter.id": 1,
  "inventory[]": [
    {}
  ],
  "inventory[].id": 1,
  "inventory[].quantity": 1,
  "inventory[].requestedAction": "Default",
  "referenceId": "RETURN101"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shipbob/latest/actions/create-return-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fulfillmentCenter": {},
    "fulfillmentCenter.id": 1,
    "inventory[]": [{}],
    "inventory[].id": 1,
    "inventory[].quantity": 1,
    "inventory[].requestedAction": "Default",
    "referenceId": "RETURN101"
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

See the full [Create Return Order action reference](actions/create-return-order.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/shipbob/latest/actions/create-return-order).
