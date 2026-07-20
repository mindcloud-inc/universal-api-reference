# Timewax Universal API Examples

These examples use the MindCloud API key and Timewax connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Authentication Token

Retrieves an authentication token from Timewax.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timewax/latest/actions/get-authentication-token?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timewax/latest/actions/get-authentication-token?${params}`, {
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
      "token": "string",
      "valid": "string",
      "validUntil": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Get Authentication Token action reference](actions/get-authentication-token.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/timewax/latest/actions/get-authentication-token).

## Create Client

Creates a new client in Timewax.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/timewax/latest/actions/create-client" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "request.company.code": "string",
  "request.company.name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/timewax/latest/actions/create-client', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "request.company.code": "string",
    "request.company.name": "Ava Chen"
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
      "valid": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Client action reference](actions/create-client.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/timewax/latest/actions/create-client).
