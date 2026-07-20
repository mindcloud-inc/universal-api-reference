# Reloadify Universal API Examples

These examples use the MindCloud API key and Reloadify connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Languages

Retrieves languages from Reloadify.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reloadify/latest/actions/list-languages?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reloadify/latest/actions/list-languages?${params}`, {
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
      "active": true,
      "code": "string",
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [List Languages action reference](actions/list-languages.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/reloadify/latest/actions/list-languages).

## Add Product To Cart

Adds a product to a shopping cart in Reloadify.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/reloadify/latest/actions/add-product-to-cart" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "languageId": "string",
  "shoppingCartId": "string",
  "productId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/reloadify/latest/actions/add-product-to-cart', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "languageId": "string",
    "shoppingCartId": "string",
    "productId": "string"
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
      "product_id": "string",
      "shopping_cart_id": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Product To Cart action reference](actions/add-product-to-cart.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/reloadify/latest/actions/add-product-to-cart).
