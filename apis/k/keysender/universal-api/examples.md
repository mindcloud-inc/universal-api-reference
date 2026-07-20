# Keysender Universal API Examples

These examples use the MindCloud API key and Keysender connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Products

Retrieves products from Keysender.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/keysender/latest/actions/list-products?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/keysender/latest/actions/list-products?${params}`, {
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
      "docs": [
        {}
      ],
      "itemsPerPage": 1,
      "page": 1,
      "total": 1,
      "totalAll": 1
    }
  ],
  "meta": {}
}
```

See the full [List Products action reference](actions/list-products.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/keysender/latest/actions/list-products).

## Add Custom Transaction

Creates a custom transaction in Keysender.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/keysender/latest/actions/add-custom-transaction" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/keysender/latest/actions/add-custom-transaction', {
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
      "amount": 1,
      "currency": "string",
      "id": 1,
      "keysenderBuyerEmail": "ava@example.com",
      "name": "Ava Chen",
      "platform": 1,
      "quantity": 1,
      "quantitySent": 1,
      "status": 1,
      "statusAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Add Custom Transaction action reference](actions/add-custom-transaction.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/keysender/latest/actions/add-custom-transaction).
