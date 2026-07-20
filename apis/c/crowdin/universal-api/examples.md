# Crowdin Universal API Examples

These examples use the MindCloud API key and Crowdin connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Authenticated User

Retrieves the authenticated user from Crowdin.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/crowdin/latest/actions/get-authenticated-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/crowdin/latest/actions/get-authenticated-user?${params}`, {
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
      "email": "ava@example.com",
      "emailVerified": true,
      "fullName": "Ava Chen",
      "id": 1,
      "lastSeen": "2026-05-07T12:00:00.000Z",
      "timezone": "string",
      "twoFactor": "string",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Get Authenticated User action reference](actions/get-authenticated-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/crowdin/latest/actions/get-authenticated-user).

## Add Branch

Creates a new branch in a Crowdin project.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/crowdin/latest/actions/add-branch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": 1,
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/crowdin/latest/actions/add-branch', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": 1,
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "exportPattern": "string",
      "id": 1,
      "name": "Ava Chen",
      "priority": "string",
      "projectId": 1,
      "title": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Add Branch action reference](actions/add-branch.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/crowdin/latest/actions/add-branch).
