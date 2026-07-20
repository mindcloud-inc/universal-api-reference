# Nyckel Universal API Examples

These examples use the MindCloud API key and Nyckel connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Functions

Retrieves functions from Nyckel.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nyckel/latest/actions/list-functions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nyckel/latest/actions/list-functions?${params}`, {
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
      "id": "string",
      "input": "string",
      "name": "Ava Chen",
      "output": "string",
      "projectId": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Functions action reference](actions/list-functions.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/nyckel/latest/actions/list-functions).

## Create Field

Creates a new field in Nyckel.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/nyckel/latest/actions/create-field" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "functionId": "string",
  "name": "Ava Chen",
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nyckel/latest/actions/create-field', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "functionId": "string",
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
  "data": [
    {
      "id": "string",
      "name": "Ava Chen",
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Field action reference](actions/create-field.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/nyckel/latest/actions/create-field).
