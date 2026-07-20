# Hub Planner Universal API Examples

These examples use the MindCloud API key and Hub Planner connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Projects

Retrieves projects from Hub Planner.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hubPlanner/latest/actions/list-projects?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hubPlanner/latest/actions/list-projects?${params}`, {
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
      "_id": "string",
      "billable": true,
      "budgetCashAmount": 1,
      "budgetCurrency": "string",
      "budgetHours": 1,
      "createdDate": "2026-05-07T12:00:00.000Z",
      "end": "2026-05-07T12:00:00.000Z",
      "metadata": "string",
      "name": "Ava Chen",
      "projectCode": "string",
      "resources": [
        "string"
      ],
      "start": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "updatedDate": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [List Projects action reference](actions/list-projects.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/hubPlanner/latest/actions/list-projects).
