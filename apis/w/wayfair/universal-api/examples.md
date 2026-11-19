# Wayfair Universal API Examples

These examples use the MindCloud API key and Wayfair connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Bill of Lading



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wayfair/latest/actions/get-bill-of-lading?connectionId=$CONNECTION_ID&purchaseOrderNumber=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "purchaseOrderNumber": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wayfair/latest/actions/get-bill-of-lading?${params}`, {
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

See the full [Get Bill of Lading action reference](actions/get-bill-of-lading.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/wayfair/latest/actions/get-bill-of-lading).

## Accept Order



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/wayfair/latest/actions/accept-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wayfair/latest/actions/accept-order', {
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
  "data": [],
  "meta": {}
}
```

See the full [Accept Order action reference](actions/accept-order.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/wayfair/latest/actions/accept-order).
