# Pipeliner Cloud Universal API Examples

These examples use the MindCloud API key and Pipeliner Cloud connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Accounts

Retrieves accounts from Pipeliner Cloud.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pipelinerCloud/latest/actions/list-accounts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pipelinerCloud/latest/actions/list-accounts?${params}`, {
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
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [List Accounts action reference](actions/list-accounts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pipelinerCloud/latest/actions/list-accounts).

## Batch Upsert Products

Creates or updates products in Pipeliner Cloud in batches.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pipelinerCloud/latest/actions/batch-upsert-products" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pipelinerCloud/latest/actions/batch-upsert-products', {
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
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Batch Upsert Products action reference](actions/batch-upsert-products.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pipelinerCloud/latest/actions/batch-upsert-products).
