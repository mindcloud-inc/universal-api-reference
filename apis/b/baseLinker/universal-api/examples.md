# BaseLinker Universal API Examples

These examples use the MindCloud API key and BaseLinker connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Order Sources

Retrieves order sources from BaseLinker.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/baseLinker/latest/actions/get-order-sources?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/baseLinker/latest/actions/get-order-sources?${params}`, {
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

See the full [Get Order Sources action reference](actions/get-order-sources.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/baseLinker/latest/actions/get-order-sources).

## Add Order Product

Adds a product to an order in BaseLinker.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/baseLinker/latest/actions/add-order-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "order_id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/baseLinker/latest/actions/add-order-product', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "order_id": 1
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
      "orderProductId": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Order Product action reference](actions/add-order-product.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/baseLinker/latest/actions/add-order-product).
