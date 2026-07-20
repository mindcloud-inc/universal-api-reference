# Tailwind Universal API Examples

These examples use the MindCloud API key and Tailwind connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Accounts

Retrieves Pinterest accounts from Tailwind.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tailwind/latest/actions/list-accounts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tailwind/latest/actions/list-accounts?${params}`, {
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
      "avatarUrl": "https://example.com",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "displayName": "Ava Chen",
      "id": "string",
      "isDomainVerified": true,
      "tokenAuthorized": true,
      "userId": "string",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [List Accounts action reference](actions/list-accounts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/tailwind/latest/actions/list-accounts).

## Create Post

Creates a new post in Tailwind.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tailwind/latest/actions/create-post" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": "string",
  "mediaUrl": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tailwind/latest/actions/create-post', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": "string",
    "mediaUrl": "https://example.com"
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
      "altText": "string",
      "boardId": "string",
      "createdAt": 1,
      "description": "string",
      "id": "string",
      "isSimplifiedPin": true,
      "mediaType": "string",
      "mediaUrl": "https://example.com",
      "pinId": "string",
      "sendAt": 1,
      "sentAt": 1,
      "status": "string",
      "title": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Create Post action reference](actions/create-post.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/tailwind/latest/actions/create-post).
