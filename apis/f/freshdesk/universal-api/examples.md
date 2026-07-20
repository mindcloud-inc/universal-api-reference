# Freshdesk Universal API Examples

These examples use the MindCloud API key and Freshdesk connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Currently Authenticated Agent

Retrieves the currently authenticated agent from Freshdesk.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/freshdesk/latest/actions/get-currently-authenticated-agent?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/freshdesk/latest/actions/get-currently-authenticated-agent?${params}`, {
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
      "active": true,
      "createdAt": "string",
      "email": "ava@example.com",
      "id": 1,
      "jobTitle": "string",
      "name": "Ava Chen",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Currently Authenticated Agent action reference](actions/get-currently-authenticated-agent.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/freshdesk/latest/actions/get-currently-authenticated-agent).

## Create Company

Creates a new company in Freshdesk.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/freshdesk/latest/actions/create-company" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/freshdesk/latest/actions/create-company', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
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
      "accountTier": "string",
      "createdAt": "string",
      "description": "string",
      "domains": [
        "string"
      ],
      "id": 1,
      "industry": "string",
      "name": "Ava Chen",
      "note": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Company action reference](actions/create-company.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/freshdesk/latest/actions/create-company).
