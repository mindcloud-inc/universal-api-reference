# Switchy.io Universal API Examples

These examples use the MindCloud API key and Switchy.io connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Count Workspaces

Retrieves the workspace count from Switchy.io.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/switchyio/latest/actions/count-workspaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/switchyio/latest/actions/count-workspaces?${params}`, {
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
      "aggregate": {}
    }
  ],
  "meta": {}
}
```

See the full [Count Workspaces action reference](actions/count-workspaces.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/switchyio/latest/actions/count-workspaces).

## Bulk Update Links

Updates existing links in Switchy.io by domain and IDs.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/switchyio/latest/actions/bulk-update-links" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "domain": "string",
  "idsCsv": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/switchyio/latest/actions/bulk-update-links', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "domain": "string",
    "idsCsv": "string"
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
      "affected_rows": 1,
      "returning": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [Bulk Update Links action reference](actions/bulk-update-links.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/switchyio/latest/actions/bulk-update-links).
