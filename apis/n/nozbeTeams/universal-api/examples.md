# Nozbe Teams Universal API Examples

These examples use the MindCloud API key and Nozbe Teams connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Teams

Retrieves accessible teams from Nozbe Teams.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nozbeTeams/latest/actions/list-teams?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nozbeTeams/latest/actions/list-teams?${params}`, {
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
      "color": "string",
      "id": "string",
      "isPersonal": true,
      "isSharedTeam": true,
      "limits": "string",
      "name": "Ava Chen",
      "sidebarPosition": 1
    }
  ],
  "meta": {}
}
```

See the full [List Teams action reference](actions/list-teams.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/nozbeTeams/latest/actions/list-teams).

## Create Comment

Creates a new comment in Nozbe Teams.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/nozbeTeams/latest/actions/create-comment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "body": "string",
  "taskId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nozbeTeams/latest/actions/create-comment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "body": "string",
    "taskId": "string"
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
      "authorId": "string",
      "body": "string",
      "createdAt": 1,
      "extra": "string",
      "id": "string",
      "isDeleted": true,
      "isPinned": true,
      "isTeam": true,
      "taskId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Comment action reference](actions/create-comment.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/nozbeTeams/latest/actions/create-comment).
