# Bitly Universal API Examples

These examples use the MindCloud API key and Bitly connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Expand Bitlink

Retrieves the long URL for a Bitly bitlink.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bitly/latest/actions/expand-bitlink?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bitly/latest/actions/expand-bitlink?${params}`, {
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
      "createdAt": "string",
      "id": "string",
      "link": "https://example.com",
      "longUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Expand Bitlink action reference](actions/expand-bitlink.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/bitly/latest/actions/expand-bitlink).

## Bulk Update Group Bitlinks

Updates tags or archives multiple group bitlinks in Bitly.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/bitly/latest/actions/bulk-update-group-bitlinks" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "action": "string",
  "groupGuid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bitly/latest/actions/bulk-update-group-bitlinks', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "action": "string",
    "groupGuid": "string"
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
      "links": [
        "https://example.com"
      ]
    }
  ],
  "meta": {}
}
```

See the full [Bulk Update Group Bitlinks action reference](actions/bulk-update-group-bitlinks.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/bitly/latest/actions/bulk-update-group-bitlinks).
