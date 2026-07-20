# Dashform Universal API Examples

These examples use the MindCloud API key and Dashform connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current User

Retrieves the current user from Dashform.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dashform/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dashform/latest/actions/get-current-user?${params}`, {
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
      "emailVerified": true,
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Get Current User action reference](actions/get-current-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dashform/latest/actions/get-current-user).

## Create Form

Creates a form in Dashform.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dashform/latest/actions/create-form" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Contact Form"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dashform/latest/actions/create-form', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Contact Form"
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
      "description": "string",
      "id": "string",
      "name": "Ava Chen",
      "organization_id": "string",
      "public_id": "string",
      "type": "string",
      "updated_at": "string",
      "user_id": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Form action reference](actions/create-form.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dashform/latest/actions/create-form).
