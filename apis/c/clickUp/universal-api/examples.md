# ClickUp Universal API Examples

These examples use the MindCloud API key and ClickUp connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Authorized Workspaces

View the Workspaces available to the authenticated user.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clickUp/latest/actions/list-authorized-workspaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clickUp/latest/actions/list-authorized-workspaces?${params}`, {
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
      "avatar": "string",
      "color": "string",
      "id": "string",
      "members": [
        {
          "user": {
            "color": "string",
            "customRole": "string",
            "dateInvited": "2026-05-07T12:00:00.000Z",
            "dateJoined": "2026-05-07T12:00:00.000Z",
            "email": "ava@example.com",
            "id": 1,
            "initials": "string",
            "lastActive": "2026-05-07T12:00:00.000Z",
            "profilePicture": "string",
            "role": 1,
            "username": "Ava Chen"
          }
        }
      ],
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [List Authorized Workspaces action reference](actions/list-authorized-workspaces.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/clickUp/latest/actions/list-authorized-workspaces).

## Create List



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/clickUp/latest/actions/create-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "folderId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clickUp/latest/actions/create-list', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "folderId": "string"
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
      "assignee": {
        "color": "string",
        "id": 1,
        "initials": "string",
        "profilePicture": "string",
        "username": "Ava Chen"
      },
      "content": "string",
      "dueDate": "string",
      "dueDateTime": true,
      "folder": {
        "access": true,
        "hidden": true,
        "id": "string",
        "name": "Ava Chen"
      },
      "id": "string",
      "inboundAddress": "string",
      "name": "Ava Chen",
      "orderindex": 1,
      "priority": {
        "color": "string",
        "priority": "string"
      },
      "space": {
        "access": true,
        "id": "string",
        "name": "Ava Chen"
      },
      "startDate": "string",
      "startDateTime": "string",
      "status": {
        "color": "string",
        "hideLabel": true,
        "status": "string"
      },
      "statuses": [
        {
          "color": "string",
          "id": "string",
          "orderindex": 1,
          "status": "string",
          "type": "string"
        }
      ],
      "taskCount": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create List action reference](actions/create-list.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/clickUp/latest/actions/create-list).
