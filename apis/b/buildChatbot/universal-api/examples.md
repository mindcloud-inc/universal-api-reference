# BuildChatbot Universal API Examples

These examples use the MindCloud API key and BuildChatbot connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Tenant Bots

Retrieves tenant bot records from BuildChatbot.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/buildChatbot/latest/actions/list-tenant-bots?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/buildChatbot/latest/actions/list-tenant-bots?${params}`, {
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

See the full [List Tenant Bots action reference](actions/list-tenant-bots.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/buildChatbot/latest/actions/list-tenant-bots).

## Create User Via Form

Creates a user in BuildChatbot via form signup.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/buildChatbot/latest/actions/create-user-via-form" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/buildChatbot/latest/actions/create-user-via-form', {
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
      "data": {},
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create User Via Form action reference](actions/create-user-via-form.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/buildChatbot/latest/actions/create-user-via-form).
