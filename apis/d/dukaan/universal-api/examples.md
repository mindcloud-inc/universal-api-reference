# Dukaan Universal API Examples

These examples use the MindCloud API key and Dukaan connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Products

Retrieves products from a Dukaan store.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dukaan/latest/actions/list-products?connectionId=$CONNECTION_ID&limit=25&offset=0&storeUuid=your-store-uuid" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "storeUuid": "your-store-uuid"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dukaan/latest/actions/list-products?${params}`, {
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
      "all_images": [
        "string"
      ],
      "base_qty": 1,
      "categories_data": [
        {}
      ],
      "created_at": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "image": "string",
      "in_stock": true,
      "inventory_quantity": 1,
      "is_active": true,
      "name": "Ava Chen",
      "original_price": 1,
      "selling_price": 1,
      "slug": "string",
      "unit": "string",
      "uuid": "string",
      "web_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [List Products action reference](actions/list-products.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dukaan/latest/actions/list-products).

## Add Customer Tag

Adds a tag to a customer in Dukaan.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dukaan/latest/actions/add-customer-tag" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "storeUuid": "your-store-uuid",
  "tag": "90198",
  "objectId": "21881957",
  "contentType": "storelead"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dukaan/latest/actions/add-customer-tag', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "storeUuid": "your-store-uuid",
    "tag": "90198",
    "objectId": "21881957",
    "contentType": "storelead"
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
      "content_type": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "modified_at": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "object_id": 1,
      "tag": 1,
      "tag_for": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Customer Tag action reference](actions/add-customer-tag.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dukaan/latest/actions/add-customer-tag).
