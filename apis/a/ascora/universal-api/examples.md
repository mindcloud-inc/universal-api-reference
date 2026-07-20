# Ascora Universal API Examples

These examples use the MindCloud API key and Ascora connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Labour Roles

Retrieves available labour roles from Ascora.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ascora/latest/actions/list-labour-roles?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ascora/latest/actions/list-labour-roles?${params}`, {
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

See the full [List Labour Roles action reference](actions/list-labour-roles.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/ascora/latest/actions/list-labour-roles).

## Add Kits To Quote

Adds kits to a quote in Ascora.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/ascora/latest/actions/add-kits-to-quote" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ascora/latest/actions/add-kits-to-quote', {
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

See the full [Add Kits To Quote action reference](actions/add-kits-to-quote.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/ascora/latest/actions/add-kits-to-quote).
