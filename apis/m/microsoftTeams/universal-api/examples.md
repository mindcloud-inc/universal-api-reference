# Microsoft Teams Universal API Examples

These examples use the MindCloud API key and Microsoft Teams connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Joined Teams

Retrieves teams you've joined in Microsoft Teams.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoftTeams/latest/actions/list-joined-teams?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoftTeams/latest/actions/list-joined-teams?${params}`, {
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
      "classification": "string",
      "createdDateTime": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "displayName": "Ava Chen",
      "id": "string",
      "isArchived": true,
      "specialization": "string",
      "tenantId": "string",
      "visibility": "string",
      "webUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [List Joined Teams action reference](actions/list-joined-teams.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/microsoftTeams/latest/actions/list-joined-teams).

## Create Channel

Creates a new channel in Microsoft Teams.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/microsoftTeams/latest/actions/create-channel" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "teamId": "string",
  "displayName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoftTeams/latest/actions/create-channel', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "teamId": "string",
    "displayName": "Ava Chen"
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
      "createdDateTime": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "displayName": "Ava Chen",
      "email": "ava@example.com",
      "id": "string",
      "isArchived": true,
      "isFavoriteByDefault": true,
      "membershipType": "string",
      "tenantId": "string",
      "webUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Create Channel action reference](actions/create-channel.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/microsoftTeams/latest/actions/create-channel).
