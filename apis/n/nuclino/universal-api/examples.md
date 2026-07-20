# Nuclino Universal API Examples

These examples use the MindCloud API key and Nuclino connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List teams

Retrieves a list of teams from Nuclino.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nuclino/latest/actions/list-teams?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nuclino/latest/actions/list-teams?${params}`, {
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

See the full [List teams action reference](actions/list-teams.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/nuclino/latest/actions/list-teams).

## Create item or collection

Creates a new item or collection in Nuclino.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/nuclino/latest/actions/create-item-or-collection" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nuclino/latest/actions/create-item-or-collection', {
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
  "data": [],
  "meta": {}
}
```

See the full [Create item or collection action reference](actions/create-item-or-collection.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/nuclino/latest/actions/create-item-or-collection).
