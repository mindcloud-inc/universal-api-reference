# v0 Universal API Examples

These examples use the MindCloud API key and v0 connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get User

Retrieves the current user from v0.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/v0/latest/actions/get-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/v0/latest/actions/get-user?${params}`, {
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
      "avatar": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "id": "string",
      "object": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get User action reference](actions/get-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/v0/latest/actions/get-user).

## Create Chat

Creates a new chat in v0.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/v0/latest/actions/create-chat" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "message": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/v0/latest/actions/create-chat', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "message": "string"
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
      "apiUrl": "https://example.com",
      "authorId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "favorite": true,
      "id": "string",
      "metadata": {},
      "modelConfiguration": {
        "imageGenerations": true,
        "modelId": "string",
        "thinking": true
      },
      "name": "Ava Chen",
      "object": "string",
      "permissions": {
        "write": true
      },
      "privacy": "string",
      "projectId": "string",
      "shareable": true,
      "title": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com",
      "webUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Create Chat action reference](actions/create-chat.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/v0/latest/actions/create-chat).
