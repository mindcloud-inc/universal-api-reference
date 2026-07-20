# Nango Universal API Examples

These examples use the MindCloud API key and Nango connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Integrations



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nango/latest/actions/list-integrations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nango/latest/actions/list-integrations?${params}`, {
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
      "displayName": "Ava Chen",
      "logo": "string",
      "provider": "string",
      "uniqueKey": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Integrations action reference](actions/list-integrations.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/nango/latest/actions/list-integrations).

## Create Connect Session



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/nango/latest/actions/create-connect-session" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nango/latest/actions/create-connect-session', {
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
      "connectLink": "https://example.com",
      "expiresAt": "string",
      "token": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Connect Session action reference](actions/create-connect-session.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/nango/latest/actions/create-connect-session).
