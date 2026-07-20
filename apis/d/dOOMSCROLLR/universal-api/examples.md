# DOOMSCROLLR Universal API Examples

These examples use the MindCloud API key and DOOMSCROLLR connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Content Posts



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dOOMSCROLLR/latest/actions/list-content-posts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dOOMSCROLLR/latest/actions/list-content-posts?${params}`, {
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

See the full [List Content Posts action reference](actions/list-content-posts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dOOMSCROLLR/latest/actions/list-content-posts).

## Create Audience Member



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dOOMSCROLLR/latest/actions/create-audience-member" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dOOMSCROLLR/latest/actions/create-audience-member', {
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

See the full [Create Audience Member action reference](actions/create-audience-member.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dOOMSCROLLR/latest/actions/create-audience-member).
