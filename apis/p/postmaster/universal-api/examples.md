# Postmaster+ Universal API Examples

These examples use the MindCloud API key and Postmaster+ connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Retrieve Domains

Retrieves available domains from the Postmaster+ API.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/postmaster/latest/actions/retrieve-domains?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/postmaster/latest/actions/retrieve-domains?${params}`, {
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
      "description": "string",
      "id": "string",
      "updatedAt": "string",
      "value": "string"
    }
  ],
  "meta": {}
}
```

See the full [Retrieve Domains action reference](actions/retrieve-domains.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/postmaster/latest/actions/retrieve-domains).

## Scan Single Email

Scans a single email in Postmaster+.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/postmaster/latest/actions/scan-single-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/postmaster/latest/actions/scan-single-email', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com"
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
      "createdAt": "string",
      "email": "ava@example.com",
      "id": 1,
      "message": "string",
      "status": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

See the full [Scan Single Email action reference](actions/scan-single-email.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/postmaster/latest/actions/scan-single-email).
