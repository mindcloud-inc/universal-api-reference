# Vistaly Universal API Examples

These examples use the MindCloud API key and Vistaly connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Auth Info

Retrieves auth info from Vistaly.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vistaly/latest/actions/get-auth-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vistaly/latest/actions/get-auth-info?${params}`, {
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
      "organizationId": "string",
      "organizationName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Get Auth Info action reference](actions/get-auth-info.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/vistaly/latest/actions/get-auth-info).

## Create Card

Creates a new card in Vistaly.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/vistaly/latest/actions/create-card" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "cardTitle": "string",
  "parentId": "string",
  "parentType": "backlog"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vistaly/latest/actions/create-card', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "cardTitle": "string",
    "parentId": "string",
    "parentType": "backlog"
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
      "cardId": "string",
      "cardUrl": "https://example.com",
      "message": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Card action reference](actions/create-card.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/vistaly/latest/actions/create-card).
