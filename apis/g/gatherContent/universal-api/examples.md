# GatherContent Universal API Examples

These examples use the MindCloud API key and GatherContent connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current User



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gatherContent/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gatherContent/latest/actions/get-current-user?${params}`, {
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
      "email": "ava@example.com",
      "first_name": "Ava",
      "last_name": "Chen",
      "timezone": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Current User action reference](actions/get-current-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/gatherContent/latest/actions/get-current-user).

## Alter Structure

Updates a structure in GatherContent and applies changes to items.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/gatherContent/latest/actions/alter-structure" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "structure": "string",
  "structure_uuid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gatherContent/latest/actions/alter-structure', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "structure": "string",
    "structure_uuid": "string"
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
      "groups": [
        {}
      ],
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

See the full [Alter Structure action reference](actions/alter-structure.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/gatherContent/latest/actions/alter-structure).
