# CustomGPT.ai Universal API Examples

These examples use the MindCloud API key and CustomGPT.ai connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current User Profile

Retrieves the current user profile from CustomGPT.ai.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/customGPTai/latest/actions/get-current-user-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/customGPTai/latest/actions/get-current-user-profile?${params}`, {
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
      "currentTeamId": 1,
      "email": "ava@example.com",
      "id": 1,
      "name": "Ava Chen",
      "profilePhotoUrl": "https://example.com",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Current User Profile action reference](actions/get-current-user-profile.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/customGPTai/latest/actions/get-current-user-profile).

## Add Source

Adds a new source to a CustomGPT.ai agent.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/customGPTai/latest/actions/add-source" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": 1,
  "sitemapPath": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/customGPTai/latest/actions/add-source', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": 1,
    "sitemapPath": "string"
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Add Source action reference](actions/add-source.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/customGPTai/latest/actions/add-source).
