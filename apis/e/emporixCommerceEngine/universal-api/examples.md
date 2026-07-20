# Emporix Commerce Engine Universal API Examples

These examples use the MindCloud API key and Emporix Commerce Engine connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Products

Retrieves products from Emporix Commerce Engine.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/emporixCommerceEngine/latest/actions/list-products?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/emporixCommerceEngine/latest/actions/list-products?${params}`, {
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
      "brandId": "string",
      "categoryIds": [
        "string"
      ],
      "code": "string",
      "description": "string",
      "id": "string",
      "labelIds": [
        "string"
      ],
      "metadata": {},
      "name": "Ava Chen",
      "productType": "string",
      "published": true,
      "template": {},
      "yrn": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Products action reference](actions/list-products.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/emporixCommerceEngine/latest/actions/list-products).

## Add Cart Item

Adds an item to a cart in Emporix Commerce Engine.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/emporixCommerceEngine/latest/actions/add-cart-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "cartId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/emporixCommerceEngine/latest/actions/add-cart-item', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "cartId": "string"
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
      "itemId": "string",
      "yrn": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Cart Item action reference](actions/add-cart-item.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/emporixCommerceEngine/latest/actions/add-cart-item).
