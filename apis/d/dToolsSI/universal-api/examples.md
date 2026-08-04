# D-Tools SI Universal API Examples

These examples use the MindCloud API key and D-Tools SI connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Client Info

Get clients published by a SI user.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dToolsSI/latest/actions/list-client-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dToolsSI/latest/actions/list-client-info?${params}`, {
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

See the full [List Client Info action reference](actions/list-client-info.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dToolsSI/latest/actions/list-client-info).

## Archive Projects



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dToolsSI/latest/actions/archive-projects" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dToolsSI/latest/actions/archive-projects', {
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

See the full [Archive Projects action reference](actions/archive-projects.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dToolsSI/latest/actions/archive-projects).
