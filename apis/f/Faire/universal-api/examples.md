# Faire Universal API Examples

These examples use the MindCloud API key and Faire connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Orders



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/Faire/latest/actions/list-orders?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/Faire/latest/actions/list-orders?${params}`, {
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

See the full [List Orders action reference](actions/list-orders.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/Faire/latest/actions/list-orders).

## Add Shipments to Order



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/Faire/latest/actions/add-shipments-to-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "orderId": "bo_bxdmjbwxid"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/Faire/latest/actions/add-shipments-to-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "orderId": "bo_bxdmjbwxid"
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

See the full [Add Shipments to Order action reference](actions/add-shipments-to-order.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/Faire/latest/actions/add-shipments-to-order).
