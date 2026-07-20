# CheckFlow Universal API Examples

These examples use the MindCloud API key and CheckFlow connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Team Members



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/checkFlow/latest/actions/list-team-members?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/checkFlow/latest/actions/list-team-members?${params}`, {
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
      "assigneeId": 1,
      "assigneeName": "Ava Chen",
      "assigneeType": 1,
      "id": 1
    }
  ],
  "meta": {}
}
```

See the full [List Team Members action reference](actions/list-team-members.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/checkFlow/latest/actions/list-team-members).

## Add Task Assignees by Name



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/checkFlow/latest/actions/add-task-assignees-by-name" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "taskId": "5678",
  "assigneeNames[]": "MindCloud Apps",
  "isAssignedExclusively": "false",
  "deleteExistingAssignees": "true"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/checkFlow/latest/actions/add-task-assignees-by-name', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "taskId": "5678",
    "assigneeNames[]": "MindCloud Apps",
    "isAssignedExclusively": "false",
    "deleteExistingAssignees": "true"
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
      "assignees": [
        {}
      ],
      "comments": [
        {}
      ],
      "fields": [
        {}
      ],
      "tags": [
        {}
      ],
      "taskCompletedByEmail": "ava@example.com",
      "taskCompletedByName": "Ava Chen",
      "taskCompletedDateTime": "2026-05-07T12:00:00.000Z",
      "taskDueDateTime": "2026-05-07T12:00:00.000Z",
      "taskId": 1,
      "taskIsComplete": true,
      "taskIsCurrentlyHalted": true,
      "taskIsCurrentlyHidden": true,
      "taskIsHeading": true,
      "taskIsNotApplicable": true,
      "taskKey": "string",
      "taskName": "Ava Chen",
      "taskNotApplicableByEmail": "ava@example.com",
      "taskNotApplicableByName": "Ava Chen",
      "taskNotApplicableDateTime": "2026-05-07T12:00:00.000Z",
      "taskUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Add Task Assignees by Name action reference](actions/add-task-assignees-by-name.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/checkFlow/latest/actions/add-task-assignees-by-name).
