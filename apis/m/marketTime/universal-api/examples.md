# MarketTime Universal API Examples

These examples use the MindCloud API key and MarketTime connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Item Inventory



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/marketTime/latest/actions/get-item-inventory?connectionId=$CONNECTION_ID&itemId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "itemId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/marketTime/latest/actions/get-item-inventory?${params}`, {
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
  "data": [],
  "meta": {}
}
```

See the full [Get Item Inventory action reference](actions/get-item-inventory.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/marketTime/latest/actions/get-item-inventory).

## Update Item Inventory



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/marketTime/latest/actions/update-item-inventory" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "itemId": "string",
  "itemNumber": "string",
  "manufacturerId": "string",
  "name": "Ava Chen",
  "unitPrice": 1,
  "unitQuantity": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/marketTime/latest/actions/update-item-inventory', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "itemId": "string",
    "itemNumber": "string",
    "manufacturerId": "string",
    "name": "Ava Chen",
    "unitPrice": 1,
    "unitQuantity": 1
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

See the full [Update Item Inventory action reference](actions/update-item-inventory.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/marketTime/latest/actions/update-item-inventory).
