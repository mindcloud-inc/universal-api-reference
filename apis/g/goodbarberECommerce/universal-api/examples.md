# Goodbarber eCommerce Universal API Examples

These examples use the MindCloud API key and Goodbarber eCommerce connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Products



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goodbarberECommerce/latest/actions/list-products?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goodbarberECommerce/latest/actions/list-products?${params}`, {
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
      "count": 1,
      "next": "string",
      "previous": "string",
      "products": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Products action reference](actions/list-products.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/goodbarberECommerce/latest/actions/list-products).

## Create Product



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/goodbarberECommerce/latest/actions/create-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "collections[]": [
    1
  ],
  "tags[]": [
    "string"
  ],
  "setCustomSimilarProducts[]": [
    1
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/goodbarberECommerce/latest/actions/create-product', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "collections[]": [1],
    "tags[]": ["string"],
    "setCustomSimilarProducts[]": [1]
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
      "brand": "string",
      "collections": [
        {}
      ],
      "createdAt": "string",
      "id": 1,
      "productRef": "string",
      "showSimilarProducts": true,
      "slug": "string",
      "status": "string",
      "summary": "string",
      "tags": [
        "string"
      ],
      "title": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Product action reference](actions/create-product.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/goodbarberECommerce/latest/actions/create-product).
