# BugHerd Universal API Examples

These examples use the MindCloud API key and BugHerd connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Show Organization

Retrieves organization details from BugHerd.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bugHerd/latest/actions/show-organization?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bugHerd/latest/actions/show-organization?${params}`, {
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
      "id": 1,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Show Organization action reference](actions/show-organization.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/bugHerd/latest/actions/show-organization).

## Add Project Client

Adds a client to a BugHerd project.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bugHerd/latest/actions/add-project-client" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "project_id": "511891"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bugHerd/latest/actions/add-project-client', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "project_id": "511891"
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
      "allowGuestsChangeTaskStatus": true,
      "allowProjectOwnerNotifications": true,
      "allowProjectSummaryEmail": true,
      "allowTaskDoneEmail": true,
      "apiKey": "string",
      "assignGuests": true,
      "changeGuestDefaultColumn": true,
      "columns": [
        {
          "createdAt": "string",
          "id": 1,
          "name": "Ava Chen",
          "projectId": 1,
          "tasksCount": 1,
          "updatedAt": "string"
        }
      ],
      "devurl": "https://example.com",
      "guests": [
        {
          "avatarUrl": "https://example.com",
          "displayName": "Ava Chen",
          "email": "ava@example.com",
          "id": 1
        }
      ],
      "guestsSeeGuests": true,
      "id": 1,
      "isActive": true,
      "isPublic": true,
      "members": [
        {
          "avatarUrl": "https://example.com",
          "displayName": "Ava Chen",
          "email": "ava@example.com",
          "id": 1
        }
      ],
      "name": "Ava Chen",
      "ownerName": {},
      "sites": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

See the full [Add Project Client action reference](actions/add-project-client.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/bugHerd/latest/actions/add-project-client).
