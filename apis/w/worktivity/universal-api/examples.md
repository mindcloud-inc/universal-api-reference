# Worktivity Universal API Examples

These examples use the MindCloud API key and Worktivity connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Teams

Retrieves teams from Worktivity with optional filters.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/worktivity/latest/actions/list-teams?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/worktivity/latest/actions/list-teams?${params}`, {
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
      "color": "string",
      "createDate": "2026-05-07T12:00:00.000Z",
      "employeeCount": 1,
      "id": "string",
      "title": "string",
      "updateDate": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [List Teams action reference](actions/list-teams.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/worktivity/latest/actions/list-teams).

## Block or Unblock Employee

Blocks or unblocks an employee in Worktivity.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/worktivity/latest/actions/block-or-unblock-employee" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/worktivity/latest/actions/block-or-unblock-employee', {
  method: 'PUT',
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
      "blocked": true
    }
  ],
  "meta": {}
}
```

See the full [Block or Unblock Employee action reference](actions/block-or-unblock-employee.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/worktivity/latest/actions/block-or-unblock-employee).
