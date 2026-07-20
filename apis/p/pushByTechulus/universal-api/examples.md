# Push by Techulus Universal API Examples

These examples use the MindCloud API key and Push by Techulus connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Invite User to Team



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pushByTechulus/latest/actions/invite-user-to-team" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "team": "string",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pushByTechulus/latest/actions/invite-user-to-team', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "team": "string",
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
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Invite User to Team action reference](actions/invite-user-to-team.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pushByTechulus/latest/actions/invite-user-to-team).
