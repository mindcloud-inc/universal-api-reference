# Pushbullet Universal API Examples

These examples use the MindCloud API key and Pushbullet connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current User

Retrieves the current user from Pushbullet.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pushBullet/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pushBullet/latest/actions/get-current-user?${params}`, {
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
      "active": true,
      "created": 1,
      "email": "ava@example.com",
      "emailNormalized": "ava@example.com",
      "iden": "string",
      "imageUrl": "https://example.com",
      "maxUploadSize": 1,
      "modified": 1,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Get Current User action reference](actions/get-current-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pushBullet/latest/actions/get-current-user).

## Create Chat

Creates a new chat in Pushbullet.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pushBullet/latest/actions/create-chat" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pushBullet/latest/actions/create-chat', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com"
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
      "active": true,
      "created": 1,
      "email": "ava@example.com",
      "iden": "string",
      "modified": 1,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Create Chat action reference](actions/create-chat.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pushBullet/latest/actions/create-chat).
