# UserCheck Universal API Examples

These examples use the MindCloud API key and UserCheck connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Status

Retrieves account status details from UserCheck.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/userCheck/latest/actions/get-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/userCheck/latest/actions/get-status?${params}`, {
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
      "account": {},
      "status": "string",
      "usage": {}
    }
  ],
  "meta": {}
}
```

See the full [Get Status action reference](actions/get-status.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/userCheck/latest/actions/get-status).

## Add Domain to Blocklist

Adds a domain to the UserCheck blocklist.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/userCheck/latest/actions/add-domain-to-blocklist" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "domain": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/userCheck/latest/actions/add-domain-to-blocklist', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "domain": "string"
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
      "created_at": "string",
      "domain": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Domain to Blocklist action reference](actions/add-domain-to-blocklist.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/userCheck/latest/actions/add-domain-to-blocklist).
