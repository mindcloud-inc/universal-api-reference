# Corporate Merch Universal API Examples

These examples use the MindCloud API key and Corporate Merch connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Catalog

Retrieves catalog products from Corporate Merch.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/corporateMerch/latest/actions/list-catalog?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/corporateMerch/latest/actions/list-catalog?${params}`, {
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
      "estimatedShipDate": "string",
      "id": "string",
      "name": "Ava Chen",
      "quantity": 1,
      "unitPrice": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Catalog action reference](actions/list-catalog.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/corporateMerch/latest/actions/list-catalog).

## Assign Designs To Organization

Assigns designs to an organization in Corporate Merch.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/corporateMerch/latest/actions/assign-designs-to-organization" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/corporateMerch/latest/actions/assign-designs-to-organization', {
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

See the full [Assign Designs To Organization action reference](actions/assign-designs-to-organization.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/corporateMerch/latest/actions/assign-designs-to-organization).
