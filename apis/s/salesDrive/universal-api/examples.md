# SalesDrive Universal API Examples

These examples use the MindCloud API key and SalesDrive connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Order Statuses

Retrieves available order statuses from SalesDrive.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salesDrive/latest/actions/list-order-statuses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/salesDrive/latest/actions/list-order-statuses?${params}`, {
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
      "id": 1,
      "name": "Ava Chen",
      "type": 1
    }
  ],
  "meta": {}
}
```

See the full [List Order Statuses action reference](actions/list-order-statuses.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/salesDrive/latest/actions/list-order-statuses).

## Add Order Note

Adds a note to an order in SalesDrive.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/salesDrive/latest/actions/add-order-note" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "orderId": 1,
  "text": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/salesDrive/latest/actions/add-order-note', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "orderId": 1,
    "text": "string"
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
      "noteId": 1,
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Add Order Note action reference](actions/add-order-note.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/salesDrive/latest/actions/add-order-note).
