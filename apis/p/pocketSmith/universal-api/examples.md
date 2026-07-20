# PocketSmith Universal API Examples

These examples use the MindCloud API key and PocketSmith connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Authorised User

Retrieves the authorised PocketSmith user.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pocketSmith/latest/actions/get-authorised-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pocketSmith/latest/actions/get-authorised-user?${params}`, {
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

See the full [Get Authorised User action reference](actions/get-authorised-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pocketSmith/latest/actions/get-authorised-user).

## Create Category In User

Creates a category for a PocketSmith user.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pocketSmith/latest/actions/create-category-in-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string",
  "userId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pocketSmith/latest/actions/create-category-in-user', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string",
    "userId": 1
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

See the full [Create Category In User action reference](actions/create-category-in-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pocketSmith/latest/actions/create-category-in-user).
