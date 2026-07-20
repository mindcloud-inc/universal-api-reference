# Endear Universal API Examples

These examples use the MindCloud API key and Endear connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Current Integration



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/endear/latest/actions/current-integration?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/endear/latest/actions/current-integration?${params}`, {
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
      "externalId": "string",
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Current Integration action reference](actions/current-integration.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/endear/latest/actions/current-integration).

## Assign Users To Customer



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/endear/latest/actions/assign-users-to-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "variables.id": "string",
  "variables.assigneeIds[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/endear/latest/actions/assign-users-to-customer', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "variables.id": "string",
    "variables.assigneeIds[]": ["string"]
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
      "id": "string"
    }
  ],
  "meta": {}
}
```

See the full [Assign Users To Customer action reference](actions/assign-users-to-customer.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/endear/latest/actions/assign-users-to-customer).
