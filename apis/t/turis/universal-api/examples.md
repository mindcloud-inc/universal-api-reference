# Turis Universal API Examples

These examples use the MindCloud API key and Turis connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Orders

Retrieves orders from Turis.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/turis/latest/actions/list-orders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/turis/latest/actions/list-orders?${params}`, {
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
      "casesCount": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "itemsCount": 1,
      "recEquiv": 1,
      "showRecEquiv": true,
      "status": "string",
      "type": "string",
      "uniqueId6": "string",
      "vat": 1
    }
  ],
  "meta": {}
}
```

See the full [List Orders action reference](actions/list-orders.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/turis/latest/actions/list-orders).

## Add Products to Order

Adds products to a Turis order.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/turis/latest/actions/add-products-to-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/turis/latest/actions/add-products-to-order', {
  method: 'PUT',
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
      "casesCount": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "itemsCount": 1,
      "recEquiv": 1,
      "showRecEquiv": true,
      "status": "string",
      "type": "string",
      "uniqueId6": "string",
      "vat": 1
    }
  ],
  "meta": {}
}
```

See the full [Add Products to Order action reference](actions/add-products-to-order.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/turis/latest/actions/add-products-to-order).
