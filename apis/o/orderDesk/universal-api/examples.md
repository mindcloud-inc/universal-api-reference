# Order Desk Universal API Examples

These examples use the MindCloud API key and Order Desk connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Store Settings

Retrieves store settings from Order Desk.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/orderDesk/latest/actions/get-store-settings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/orderDesk/latest/actions/get-store-settings?${params}`, {
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
      "folders": {},
      "id": 1,
      "name": "Ava Chen",
      "settings": {}
    }
  ],
  "meta": {}
}
```

See the full [Get Store Settings action reference](actions/get-store-settings.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/orderDesk/latest/actions/get-store-settings).

## Create Inventory Item

Creates a new inventory item in Order Desk.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/orderDesk/latest/actions/create-inventory-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "code": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/orderDesk/latest/actions/create-inventory-item', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "code": "string"
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
      "executionTime": "string",
      "inventoryItem": {},
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Inventory Item action reference](actions/create-inventory-item.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/orderDesk/latest/actions/create-inventory-item).
