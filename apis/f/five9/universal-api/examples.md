# Five9 Universal API Examples

These examples use the MindCloud API key and Five9 connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Campaign Settings



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/five9/latest/actions/campaign-settings?connectionId=$CONNECTION_ID&domainID=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domainID": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/five9/latest/actions/campaign-settings?${params}`, {
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

See the full [Campaign Settings action reference](actions/campaign-settings.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/five9/latest/actions/campaign-settings).

## Create User



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/five9/latest/actions/create-users" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/five9/latest/actions/create-users', {
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

See the full [Create User action reference](actions/create-users.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/five9/latest/actions/create-users).
