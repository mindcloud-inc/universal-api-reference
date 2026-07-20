# Pachca Universal API Examples

These examples use the MindCloud API key and Pachca connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get token info



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pachca/latest/actions/get-token-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pachca/latest/actions/get-token-info?${params}`, {
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
      "created_at": "2026-05-07T12:00:00.000Z",
      "expires_in": 1,
      "id": 1,
      "last_used_at": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "revoked_at": "2026-05-07T12:00:00.000Z",
      "scopes": [
        "string"
      ],
      "token": "string",
      "user_id": 1
    }
  ],
  "meta": {}
}
```

See the full [Get token info action reference](actions/get-token-info.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pachca/latest/actions/get-token-info).

## Create chat



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pachca/latest/actions/create-chat" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "chat": {},
  "chat.name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pachca/latest/actions/create-chat', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "chat": {},
    "chat.name": "Ava Chen"
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
      "channel": true,
      "created_at": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "name": "Ava Chen",
      "private": true,
      "public": true,
      "updated_at": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Create chat action reference](actions/create-chat.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pachca/latest/actions/create-chat).
