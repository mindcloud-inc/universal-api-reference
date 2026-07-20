# Quizell Universal API Examples

These examples use the MindCloud API key and Quizell connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Search Products

Finds products in Quizell by title or SKU.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quizell/latest/actions/search-products?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quizell/latest/actions/search-products?${params}`, {
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
      "bullet_description": "string",
      "collections": [
        {}
      ],
      "compare_at_price": 1,
      "created_at": "string",
      "description": "string",
      "detail_link": "https://example.com",
      "id": 1,
      "image": "string",
      "images": [
        {}
      ],
      "price": "string",
      "sku": "string",
      "status": true,
      "tags": [
        "string"
      ],
      "title": "string",
      "updated_at": "string",
      "vendor": "string"
    }
  ],
  "meta": {}
}
```

See the full [Search Products action reference](actions/search-products.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/quizell/latest/actions/search-products).

## Batch Products

Creates multiple products in Quizell.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/quizell/latest/actions/batch-products" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "products": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/quizell/latest/actions/batch-products', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "products": {}
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
      "message": "string",
      "status": true
    }
  ],
  "meta": {}
}
```

See the full [Batch Products action reference](actions/batch-products.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/quizell/latest/actions/batch-products).
