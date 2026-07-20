# Jotform Universal API Examples

These examples use the MindCloud API key and Jotform connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get User

Retrieves the current user from Jotform.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jotform/latest/actions/get-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jotform/latest/actions/get-user?${params}`, {
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
      "email": "ava@example.com",
      "is2FAEnabled": true,
      "name": "Ava Chen",
      "status": "string",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Get User action reference](actions/get-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/jotform/latest/actions/get-user).

## Create Form

Creates a form in Jotform.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/jotform/latest/actions/create-form" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/jotform/latest/actions/create-form', {
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
      "id": "string",
      "status": "string",
      "title": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Create Form action reference](actions/create-form.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/jotform/latest/actions/create-form).
