# Teyuto Universal API Examples

These examples use the MindCloud API key and Teyuto connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Users

Retrieves all users from a Teyuto account.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/teyuto/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/teyuto/latest/actions/list-users?${params}`, {
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

See the full [List Users action reference](actions/list-users.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/teyuto/latest/actions/list-users).

## Create Tag

Creates a new tag in Teyuto.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/teyuto/latest/actions/create-tag" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string",
  "description": "string",
  "privacy": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/teyuto/latest/actions/create-tag', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string",
    "description": "string",
    "privacy": "string"
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

See the full [Create Tag action reference](actions/create-tag.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/teyuto/latest/actions/create-tag).
