# Tinybird Universal API Examples

These examples use the MindCloud API key and Tinybird connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Data Sources



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tinybird/latest/actions/list-data-sources?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tinybird/latest/actions/list-data-sources?${params}`, {
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
      "datasources": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Data Sources action reference](actions/list-data-sources.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/tinybird/latest/actions/list-data-sources).

## Add Pipe Node



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tinybird/latest/actions/add-pipe-node" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "sql": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tinybird/latest/actions/add-pipe-node', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "sql": "string"
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

See the full [Add Pipe Node action reference](actions/add-pipe-node.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/tinybird/latest/actions/add-pipe-node).
