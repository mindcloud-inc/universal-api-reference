# Checkvist Universal API Examples

These examples use the MindCloud API key and Checkvist connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current User

Retrieves the current user from Checkvist.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/checkvist/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/checkvist/latest/actions/get-current-user?${params}`, {
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
      "email": "ava@example.com",
      "emailMd5": "ava@example.com",
      "id": 1,
      "pro": true,
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Get Current User action reference](actions/get-current-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/checkvist/latest/actions/get-current-user).

## Change Task Status

Updates a task status in Checkvist.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/checkvist/latest/actions/change-task-status" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "action": "string",
  "checklistId": 1,
  "taskId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/checkvist/latest/actions/change-task-status', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "action": "string",
    "checklistId": 1,
    "taskId": 1
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
      "assigneeIds": [
        1
      ],
      "backlinkIds": [
        1
      ],
      "checklistId": 1,
      "collapsed": true,
      "commentsCount": 1,
      "content": "string",
      "createdAt": "string",
      "details": {},
      "due": "string",
      "id": 1,
      "linkIds": [
        1
      ],
      "parentId": 1,
      "position": 1,
      "priority": 1,
      "status": 1,
      "tags": {},
      "tagsAsText": "string",
      "tasks": [
        1
      ],
      "updatedAt": "string",
      "updateLine": "string"
    }
  ],
  "meta": {}
}
```

See the full [Change Task Status action reference](actions/change-task-status.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/checkvist/latest/actions/change-task-status).
