# Chatrace Universal API Examples

These examples use the MindCloud API key and Chatrace connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Account Tags

Retrieves account tags from your Chatrace account.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatrace/latest/actions/list-account-tags?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatrace/latest/actions/list-account-tags?${params}`, {
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
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [List Account Tags action reference](actions/list-account-tags.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/chatrace/latest/actions/list-account-tags).

## Add Product To Cart

Adds a product to a Chatrace contact cart.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chatrace/latest/actions/add-product-to-cart" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatrace/latest/actions/add-product-to-cart', {
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
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Add Product To Cart action reference](actions/add-product-to-cart.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/chatrace/latest/actions/add-product-to-cart).
