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
  "data": [],
  "meta": {}
}
```

See the full [List Inventory Levels by Location action reference](actions/list-inventory-levels-by-location.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/shipbob/latest/actions/list-inventory-levels-by-location).

## Post Product



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/shipbob/latest/actions/post-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shipbob/latest/actions/post-product', {
  method: 'POST',
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

See the full [Post Product action reference](actions/post-product.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/shipbob/latest/actions/post-product).
