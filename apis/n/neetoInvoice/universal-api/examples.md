# NeetoInvoice Universal API Examples

These examples use the MindCloud API key and NeetoInvoice connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Team Members

Retrieves all team members from NeetoInvoice.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/neetoInvoice/latest/actions/list-team-members?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/neetoInvoice/latest/actions/list-team-members?${params}`, {
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
      "pagination": {
        "currentPageNumber": 1,
        "pageSize": 1,
        "totalPages": 1,
        "totalRecords": 1
      },
      "teamMembers": [
        {
          "active": true,
          "email": "ava@example.com",
          "firstName": "Ava",
          "id": "string",
          "lastName": "Chen",
          "organizationRole": "string",
          "profileImageUrl": "https://example.com",
          "timeZone": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Team Members action reference](actions/list-team-members.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/neetoInvoice/latest/actions/list-team-members).

## Add Project User

Adds a user to a project in NeetoInvoice.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/neetoInvoice/latest/actions/add-project-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/neetoInvoice/latest/actions/add-project-user', {
  method: 'POST',
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
      "projectUser": {
        "id": "string",
        "projectId": "string",
        "role": "string",
        "userId": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [Add Project User action reference](actions/add-project-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/neetoInvoice/latest/actions/add-project-user).
