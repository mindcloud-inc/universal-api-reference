# Cloudprinter.com Universal API Examples

These examples use the MindCloud API key and Cloudprinter.com connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Products

Retrieves products from Cloudprinter.com.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudprintercom/latest/actions/list-products?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudprintercom/latest/actions/list-products?${params}`, {
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
      "availability": "string",
      "category": "string",
      "name": "Ava Chen",
      "note": "string",
      "reference": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Products action reference](actions/list-products.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/cloudprintercom/latest/actions/list-products).

## Add Order

Creates an order in Cloudprinter.com.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cloudprintercom/latest/actions/add-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "reference": "string",
  "email": "ava@example.com",
  "addresses[]": [
    {}
  ],
  "addresses[].type": "delivery",
  "addresses[].firstname": "Ava",
  "addresses[].lastname": "Chen",
  "addresses[].street1": "string",
  "addresses[].zip": "string",
  "addresses[].city": "string",
  "addresses[].country": "string",
  "addresses[].email": "ava@example.com",
  "addresses[].phone": "string",
  "items[]": [
    {}
  ],
  "items[].reference": "string",
  "items[].product": "string",
  "items[].count": "string",
  "items[].files[]": [
    {}
  ],
  "items[].files[].type": "string",
  "items[].files[].url": "https://example.com",
  "items[].files[].md5sum": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cloudprintercom/latest/actions/add-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "reference": "string",
    "email": "ava@example.com",
    "addresses[]": [{}],
    "addresses[].type": "delivery",
    "addresses[].firstname": "Ava",
    "addresses[].lastname": "Chen",
    "addresses[].street1": "string",
    "addresses[].zip": "string",
    "addresses[].city": "string",
    "addresses[].country": "string",
    "addresses[].email": "ava@example.com",
    "addresses[].phone": "string",
    "items[]": [{}],
    "items[].reference": "string",
    "items[].product": "string",
    "items[].count": "string",
    "items[].files[]": [{}],
    "items[].files[].type": "string",
    "items[].files[].url": "https://example.com",
    "items[].files[].md5sum": "string"
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
      "order": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Order action reference](actions/add-order.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/cloudprintercom/latest/actions/add-order).
