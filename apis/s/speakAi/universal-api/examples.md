# Speak Ai Universal API Examples

These examples use the MindCloud API key and Speak Ai connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Request Access Token

Requests an access token from Speak Ai.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/speakAi/latest/actions/request-access-token?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/speakAi/latest/actions/request-access-token?${params}`, {
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
      "accessToken": "string",
      "email": "ava@example.com",
      "refreshToken": "string"
    }
  ],
  "meta": {}
}
```

See the full [Request Access Token action reference](actions/request-access-token.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/speakAi/latest/actions/request-access-token).

## Create Folder

Creates a folder in Speak Ai.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/speakAi/latest/actions/create-folder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/speakAi/latest/actions/create-folder', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
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
      "folderId": "string",
      "message": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Folder action reference](actions/create-folder.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/speakAi/latest/actions/create-folder).
