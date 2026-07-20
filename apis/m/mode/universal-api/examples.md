# Mode Universal API Examples

These examples use the MindCloud API key and Mode connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Collections

List collections that are visible in a Mode workspace.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mode/latest/actions/list-collections?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mode/latest/actions/list-collections?${params}`, {
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
      "defaultAccessLevel": "string",
      "description": "string",
      "Forms": {},
      "freeDefault": true,
      "id": "string",
      "Links": {},
      "name": "Ava Chen",
      "restricted": true,
      "schemaName": "Ava Chen",
      "spaceType": "string",
      "state": "string",
      "token": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Collections action reference](actions/list-collections.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mode/latest/actions/list-collections).

## Create Collection

Create a collection in a Mode workspace.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mode/latest/actions/create-collection" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "space": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mode/latest/actions/create-collection', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "space": {}
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
      "defaultAccessLevel": "string",
      "description": "string",
      "Forms": {},
      "freeDefault": true,
      "id": "string",
      "Links": {},
      "name": "Ava Chen",
      "restricted": true,
      "schemaName": "Ava Chen",
      "spaceType": "string",
      "state": "string",
      "token": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Collection action reference](actions/create-collection.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mode/latest/actions/create-collection).
