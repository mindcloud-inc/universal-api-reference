# YouCan Universal API Examples

These examples use the MindCloud API key and YouCan connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Products

Retrieves a list of products from YouCan.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/youCan/latest/actions/list-products?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/youCan/latest/actions/list-products?${params}`, {
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
      "data": [
        {
          "compare_at_price": 1,
          "created_at": "2026-05-07T12:00:00.000Z",
          "deleted_at": true,
          "description": "string",
          "has_variants": true,
          "id": "string",
          "images": [
            {
              "id": "string",
              "name": "Ava Chen",
              "order": 1,
              "type": 1,
              "url": "https://example.com",
              "variations": {
                "lg": "string",
                "md": "string",
                "original": "string",
                "sm": "string"
              }
            }
          ],
          "inventory": 1,
          "meta": {
            "description": "string",
            "title": "string"
          },
          "name": "Ava Chen",
          "orders_count": 1,
          "price": 1,
          "public_url": "https://example.com",
          "slug": "string",
          "thumbnail": "string",
          "track_inventory": true,
          "updated_at": "2026-05-07T12:00:00.000Z",
          "variant_options": [
            {
              "name": "Ava Chen",
              "type": 1,
              "values": [
                "string"
              ]
            }
          ],
          "variants_count": 1,
          "visibility": true,
          "you_save_amount": 1
        }
      ],
      "meta": {
        "pagination": {
          "count": 1,
          "current_page": 1,
          "links": {
            "next": "https://example.com"
          },
          "per_page": 1,
          "total": 1,
          "total_pages": 1
        }
      }
    }
  ],
  "meta": {}
}
```

See the full [List Products action reference](actions/list-products.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/youCan/latest/actions/list-products).

## Close Order

Updates an order in YouCan by closing it.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/youCan/latest/actions/close-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/youCan/latest/actions/close-order', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
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
      "code": "string",
      "http_code": 1,
      "message": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Close Order action reference](actions/close-order.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/youCan/latest/actions/close-order).
