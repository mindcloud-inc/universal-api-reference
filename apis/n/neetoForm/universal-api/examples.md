# NeetoForm Universal API Examples

These examples use the MindCloud API key and NeetoForm connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Forms

Retrieves forms from a NeetoForm workspace.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/neetoForm/latest/actions/list-forms?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/neetoForm/latest/actions/list-forms?${params}`, {
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
      "forms": [
        {
          "attemptUrl": "https://example.com",
          "createdAt": "2026-05-07T12:00:00.000Z",
          "createdBy": "string",
          "id": "string",
          "isArchived": true,
          "isDisabled": true,
          "isPublished": true,
          "isSuspended": true,
          "state": "string",
          "submissionsCount": 1,
          "title": "string",
          "updatedAt": "2026-05-07T12:00:00.000Z"
        }
      ],
      "pagination": {
        "currentPageNumber": 1,
        "pageSize": 1,
        "totalPages": 1,
        "totalRecords": 1
      },
      "totalCount": 1
    }
  ],
  "meta": {}
}
```

See the full [List Forms action reference](actions/list-forms.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/neetoForm/latest/actions/list-forms).

## Add Team Members

Adds team members to a NeetoForm workspace.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/neetoForm/latest/actions/add-team-members" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "emails[]": [
    "ava@example.com"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/neetoForm/latest/actions/add-team-members', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "emails[]": ["ava@example.com"]
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
      "message": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Team Members action reference](actions/add-team-members.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/neetoForm/latest/actions/add-team-members).
