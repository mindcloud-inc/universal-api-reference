# LiveWebinar Universal API Examples

These examples use the MindCloud API key and LiveWebinar connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Me

Retrieves the authenticated user from LiveWebinar.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/liveWebinar/latest/actions/get-me?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/liveWebinar/latest/actions/get-me?${params}`, {
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

See the full [Get Me action reference](actions/get-me.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/liveWebinar/latest/actions/get-me).

## Create Form

Creates a new form in LiveWebinar.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/liveWebinar/latest/actions/create-form" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/liveWebinar/latest/actions/create-form', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "type": "string"
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

See the full [Create Form action reference](actions/create-form.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/liveWebinar/latest/actions/create-form).
