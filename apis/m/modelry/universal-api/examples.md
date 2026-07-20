# Modelry Universal API Examples

These examples use the MindCloud API key and Modelry connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Workspaces



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/modelry/latest/actions/list-workspaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/modelry/latest/actions/list-workspaces?${params}`, {
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
      "attributes": {
        "name": "Ava Chen"
      },
      "id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Workspaces action reference](actions/list-workspaces.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/modelry/latest/actions/list-workspaces).

## Create Blob



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/modelry/latest/actions/create-blob" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "blob.filename": "Ava Chen",
  "blob.byteSize": 1,
  "blob.checksum": "string",
  "blob.contentType": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/modelry/latest/actions/create-blob', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "blob.filename": "Ava Chen",
    "blob.byteSize": 1,
    "blob.checksum": "string",
    "blob.contentType": "string"
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

See the full [Create Blob action reference](actions/create-blob.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/modelry/latest/actions/create-blob).
