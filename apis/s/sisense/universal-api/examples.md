# Sisense Universal API Examples

These examples use the MindCloud API key and Sisense connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Users

Retrieves users from a Sisense instance.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sisense/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sisense/latest/actions/list-users?${params}`, {
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

See the full [List Users action reference](actions/list-users.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sisense/latest/actions/list-users).

## Add Custom Column To Table

Adds a custom column to a Sisense table.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sisense/latest/actions/add-custom-column-to-table" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sisense/latest/actions/add-custom-column-to-table', {
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
  "data": [],
  "meta": {}
}
```

See the full [Add Custom Column To Table action reference](actions/add-custom-column-to-table.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sisense/latest/actions/add-custom-column-to-table).
