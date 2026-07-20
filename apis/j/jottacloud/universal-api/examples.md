# Jottacloud Universal API Examples

These examples use the MindCloud API key and Jottacloud connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Userinfo



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jottacloud/latest/actions/get-userinfo?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jottacloud/latest/actions/get-userinfo?${params}`, {
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

See the full [Get Userinfo action reference](actions/get-userinfo.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/jottacloud/latest/actions/get-userinfo).

## Copy Path



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/jottacloud/latest/actions/copy-path" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "from_path": "string",
  "to_path": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/jottacloud/latest/actions/copy-path', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "from_path": "string",
    "to_path": "string"
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

See the full [Copy Path action reference](actions/copy-path.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/jottacloud/latest/actions/copy-path).
