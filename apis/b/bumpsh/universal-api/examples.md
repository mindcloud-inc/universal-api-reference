# Bump.sh Universal API Examples

These examples use the MindCloud API key and Bump.sh connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Hubs

Retrieves hubs from Bump.sh.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bumpsh/latest/actions/list-hubs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bumpsh/latest/actions/list-hubs?${params}`, {
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

See the full [List Hubs action reference](actions/list-hubs.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/bumpsh/latest/actions/list-hubs).

## Create Branch

Creates a new branch in Bump.sh.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bumpsh/latest/actions/create-branch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "doc_id_or_slug": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bumpsh/latest/actions/create-branch', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "doc_id_or_slug": "string",
    "name": "Ava Chen"
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

See the full [Create Branch action reference](actions/create-branch.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/bumpsh/latest/actions/create-branch).
