# Evervault Universal API Examples

These examples use the MindCloud API key and Evervault connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Relays

Retrieves all configured relays from Evervault.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/evervault/latest/actions/list-relays?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/evervault/latest/actions/list-relays?${params}`, {
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
      "data": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Relays action reference](actions/list-relays.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/evervault/latest/actions/list-relays).

## Create Client Token

Creates a client token in Evervault.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/evervault/latest/actions/create-client-token" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/evervault/latest/actions/create-client-token', {
  method: 'POST',
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
      "createdAt": 1,
      "expiry": 1,
      "id": "string",
      "token": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Client Token action reference](actions/create-client-token.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/evervault/latest/actions/create-client-token).
