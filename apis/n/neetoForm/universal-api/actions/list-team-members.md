# NeetoForm: List Team Members

Retrieves team members from a NeetoForm workspace.

```
GET https://connect.mindcloud.co/v1/universal/neetoForm/latest/actions/list-team-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NeetoForm `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/neetoForm/latest/actions/list-team-members?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/neetoForm/latest/actions/list-team-members?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

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
          "createdAt": "2026-05-07T12:00:00.000Z",
          "email": "ava@example.com",
          "firstName": "Ava",
          "id": "string",
          "lastName": "Chen",
          "organizationRole": "string",
          "timeZone": "string",
          "updatedAt": "2026-05-07T12:00:00.000Z"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `pagination.currentPageNumber` | number |  |
| `pagination.pageSize` | number |  |
| `pagination.totalPages` | number |  |
| `pagination.totalRecords` | number |  |
| `teamMembers[].active` | boolean |  |
| `teamMembers[].createdAt` | date |  |
| `teamMembers[].email` | string |  |
| `teamMembers[].firstName` | string |  |
| `teamMembers[].id` | string |  |
| `teamMembers[].lastName` | string |  |
| `teamMembers[].organizationRole` | string |  |
| `teamMembers[].timeZone` | string |  |
| `teamMembers[].updatedAt` | date |  |

## Native endpoint

Through the native NeetoForm API, this operation is `GET /team_members` (base URL `https://{{credentials.workspaceSubdomain}}.neetoform.com/api/external/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-team-members.md) for the provider-specific parameters and requirements.

