# Shopkit Universal API Examples

These examples use the MindCloud API key and Shopkit connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Store

Retrieves store details from Shopkit.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shopkit/latest/actions/get-store?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shopkit/latest/actions/get-store?${params}`, {
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
      "currency": "string",
      "description": "string",
      "email": "ava@example.com",
      "enable_shipping_methods": true,
      "name": "Ava Chen",
      "navigation": {},
      "settings": {},
      "show_email": true,
      "url": "https://example.com",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Get Store action reference](actions/get-store.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/shopkit/latest/actions/get-store).

## Create Brand

Creates a new brand in Shopkit.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/shopkit/latest/actions/create-brand" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shopkit/latest/actions/create-brand', {
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
      "active": true,
      "created_at": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "handle": "string",
      "id": 1,
      "image": {},
      "num_products": 1,
      "permalink": "https://example.com",
      "title": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Create Brand action reference](actions/create-brand.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/shopkit/latest/actions/create-brand).
