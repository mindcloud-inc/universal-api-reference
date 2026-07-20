# Parklio Universal API Examples

These examples use the MindCloud API key and Parklio connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Products

Retrieves products from Parklio.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/parklio/latest/actions/list-products?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/parklio/latest/actions/list-products?${params}`, {
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
  "data": [],
  "meta": {}
}
```

See the full [List Products action reference](actions/list-products.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/parklio/latest/actions/list-products).

## Update Lot Description

Updates a lot description in Parklio.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/parklio/latest/actions/update-lot-description" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "description": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/parklio/latest/actions/update-lot-description', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "description": "string"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [],
  "meta": {}
}
```

See the full [Update Lot Description action reference](actions/update-lot-description.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/parklio/latest/actions/update-lot-description).
