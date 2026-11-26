# eBay Universal API Examples

These examples use the MindCloud API key and eBay connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Inventory Items



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ebay/latest/actions/list-inventory-items?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ebay/latest/actions/list-inventory-items?${params}`, {
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
      "availability": {
        "shipToLocationAvailability": {
          "quantity": 1
        }
      },
      "condition": "string",
      "conditionDescription": "string",
      "locale": "string",
      "product": {
        "brand": "string",
        "description": "string",
        "imageUrls": [
          "https://example.com"
        ],
        "mpn": "string",
        "subtitle": "string",
        "title": "string"
      },
      "sku": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Inventory Items action reference](actions/list-inventory-items.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/ebay/latest/actions/list-inventory-items).

## Bulk Migrate Listings

Create a new Inventory Location.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ebay/latest/actions/bulk-migrate-listings" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ebay/latest/actions/bulk-migrate-listings', {
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

See the full [Bulk Migrate Listings action reference](actions/bulk-migrate-listings.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/ebay/latest/actions/bulk-migrate-listings).
