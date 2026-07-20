# Everbill Universal API Examples

These examples use the MindCloud API key and Everbill connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Articles

Retrieves articles from Everbill.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/everbill/latest/actions/list-articles?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/everbill/latest/actions/list-articles?${params}`, {
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

See the full [List Articles action reference](actions/list-articles.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/everbill/latest/actions/list-articles).

## Add Bill Item

Creates a new bill item in Everbill.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/everbill/latest/actions/add-bill-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/everbill/latest/actions/add-bill-item', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
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

See the full [Add Bill Item action reference](actions/add-bill-item.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/everbill/latest/actions/add-bill-item).
