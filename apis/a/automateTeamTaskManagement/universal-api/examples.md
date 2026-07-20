# Automate Team - Task Management Universal API Examples

These examples use the MindCloud API key and Automate Team - Task Management connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Task Counts



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/automateTeamTaskManagement/latest/actions/get-task-counts?connectionId=$CONNECTION_ID&workspaceId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/automateTeamTaskManagement/latest/actions/get-task-counts?${params}`, {
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
      "completed_count": 1,
      "completed_in_time_count": 1,
      "delayed_count": 1,
      "in_progress_count": 1,
      "overdue_count": 1,
      "pending_count": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Task Counts action reference](actions/get-task-counts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/automateTeamTaskManagement/latest/actions/get-task-counts).
