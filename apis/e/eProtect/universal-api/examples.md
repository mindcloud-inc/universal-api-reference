# 3E Protect Universal API Examples

These examples use the MindCloud API key and 3E Protect connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Locations



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eProtect/latest/actions/list-locations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eProtect/latest/actions/list-locations?${params}`, {
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

See the full [List Locations action reference](actions/list-locations.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/eProtect/latest/actions/list-locations).

## Add Catalog Item Identifiers



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/eProtect/latest/actions/add-catalog-item-identifiers" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "source": "string",
  "identifier": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eProtect/latest/actions/add-catalog-item-identifiers', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "source": "string",
    "identifier": "string"
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

See the full [Add Catalog Item Identifiers action reference](actions/add-catalog-item-identifiers.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/eProtect/latest/actions/add-catalog-item-identifiers).
