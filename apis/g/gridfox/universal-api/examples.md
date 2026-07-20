# Gridfox Universal API Examples

These examples use the MindCloud API key and Gridfox connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Tables

Retrieves tables in a Gridfox project.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gridfox/latest/actions/list-tables?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gridfox/latest/actions/list-tables?${params}`, {
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
      "fields": [
        {}
      ],
      "name": "Ava Chen",
      "referenceFieldName": "Ava Chen",
      "singularName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [List Tables action reference](actions/list-tables.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/gridfox/latest/actions/list-tables).

## Add User

Adds a user to a Gridfox project.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/gridfox/latest/actions/add-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gridfox/latest/actions/add-user', {
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
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Add User action reference](actions/add-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/gridfox/latest/actions/add-user).
