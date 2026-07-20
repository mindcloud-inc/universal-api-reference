# Typesense Universal API Examples

These examples use the MindCloud API key and Typesense connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Health

Retrieves current cluster health from Typesense.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/typesense/latest/actions/get-health?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/typesense/latest/actions/get-health?${params}`, {
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
      "ok": true,
      "response": {}
    }
  ],
  "meta": {}
}
```

See the full [Get Health action reference](actions/get-health.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/typesense/latest/actions/get-health).

## Clear Cache

Clears the current server cache in Typesense.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/typesense/latest/actions/clear-cache" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/typesense/latest/actions/clear-cache', {
  method: 'PUT',
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
      "response": {},
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Clear Cache action reference](actions/clear-cache.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/typesense/latest/actions/clear-cache).
