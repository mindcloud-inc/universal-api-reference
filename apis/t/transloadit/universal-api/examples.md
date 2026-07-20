# Transloadit Universal API Examples

These examples use the MindCloud API key and Transloadit connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Assemblies

Retrieves a list of assemblies from Transloadit.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/transloadit/latest/actions/list-assemblies?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/transloadit/latest/actions/list-assemblies?${params}`, {
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
      "count": 1,
      "items": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Assemblies action reference](actions/list-assemblies.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/transloadit/latest/actions/list-assemblies).

## Create Assembly

Creates a new assembly in Transloadit.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/transloadit/latest/actions/create-assembly" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "params": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/transloadit/latest/actions/create-assembly', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "params": "string"
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
      "assembly_id": "string",
      "assembly_ssl_url": "https://example.com",
      "message": "string",
      "ok": "string",
      "results": {},
      "uploads": [
        {}
      ],
      "websocket_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Create Assembly action reference](actions/create-assembly.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/transloadit/latest/actions/create-assembly).
