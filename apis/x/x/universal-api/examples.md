# X Universal API Examples

These examples use the MindCloud API key and X connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get My Profile



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/x/latest/actions/get-my-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/x/latest/actions/get-my-profile?${params}`, {
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

See the full [Get My Profile action reference](actions/get-my-profile.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/x/latest/actions/get-my-profile).

## Create Post



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/x/latest/actions/create-post" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/x/latest/actions/create-post', {
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

See the full [Create Post action reference](actions/create-post.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/x/latest/actions/create-post).
