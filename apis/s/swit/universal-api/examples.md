# Swit Universal API Examples

These examples use the MindCloud API key and Swit connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Teams

Retrieves teams and member IDs from Swit.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/swit/latest/actions/list-teams?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/swit/latest/actions/list-teams?${params}`, {
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
      "depth": 1,
      "member_cnt": 1,
      "parent_id": "string",
      "reference": "string",
      "team_id": "string",
      "team_name": "Ava Chen",
      "users": [
        [
          "string"
        ]
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Teams action reference](actions/list-teams.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/swit/latest/actions/list-teams).

## Add Users To Team

Adds users to a team in Swit.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/swit/latest/actions/add-users-to-team" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "teamId": "string",
  "userIds[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/swit/latest/actions/add-users-to-team', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "teamId": "string",
    "userIds[]": ["string"]
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
      "depth": 1,
      "member_cnt": 1,
      "parent_id": "string",
      "reference": "string",
      "team_id": "string",
      "team_name": "Ava Chen",
      "users": [
        [
          "string"
        ]
      ]
    }
  ],
  "meta": {}
}
```

See the full [Add Users To Team action reference](actions/add-users-to-team.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/swit/latest/actions/add-users-to-team).
