# BASIC Universal API Examples

These examples use the MindCloud API key and BASIC connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get all admin projects of developer

Retrieves admin projects for the current developer in BASIC.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bASIC/latest/actions/list-admin-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bASIC/latest/actions/list-admin-projects?${params}`, {
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
      "data": [
        {
          "created_at": "2026-05-07T12:00:00.000Z",
          "id": "string",
          "name": "Ava Chen",
          "profile": {
            "icon_url": "https://example.com",
            "styles": {
              "background_url": "https://example.com"
            }
          },
          "slug": "string",
          "team_id": "string",
          "team_name": "Ava Chen",
          "team_slug": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

See the full [Get all admin projects of developer action reference](actions/list-admin-projects.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/bASIC/latest/actions/list-admin-projects).

## Accept a team invite

Accepts a team invite in BASIC.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bASIC/latest/actions/accept-a-team-invite" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bASIC/latest/actions/accept-a-team-invite', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
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
      "data": {
        "account_id": "string",
        "role_name": "Ava Chen",
        "roles": "string",
        "team_id": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [Accept a team invite action reference](actions/accept-a-team-invite.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/bASIC/latest/actions/accept-a-team-invite).
