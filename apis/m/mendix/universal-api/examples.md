# Mendix Universal API Examples

These examples use the MindCloud API key and Mendix connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Projects

Retrieves company-owned projects from Mendix.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mendix/latest/actions/list-projects?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mendix/latest/actions/list-projects?${params}`, {
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
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [List Projects action reference](actions/list-projects.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mendix/latest/actions/list-projects).

## Add Project Member

Adds a project team member in Mendix or sends an invitation.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mendix/latest/actions/add-project-member" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "d92064a5-b1fd-4be4-97db-53fc90201d1c"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mendix/latest/actions/add-project-member', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "d92064a5-b1fd-4be4-97db-53fc90201d1c"
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
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Add Project Member action reference](actions/add-project-member.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mendix/latest/actions/add-project-member).
