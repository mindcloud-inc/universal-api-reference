# NeetoInvoice: List Team Members

Retrieves all team members from NeetoInvoice.

```
GET https://connect.mindcloud.co/v1/universal/neetoInvoice/latest/actions/list-team-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NeetoInvoice `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

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

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `pagination.currentPageNumber` | number |  |
| `pagination.pageSize` | number |  |
| `pagination.totalPages` | number |  |
| `pagination.totalRecords` | number |  |
| `teamMembers[].active` | boolean |  |
| `teamMembers[].email` | string |  |
| `teamMembers[].firstName` | string |  |
| `teamMembers[].id` | string |  |
| `teamMembers[].lastName` | string |  |
| `teamMembers[].organizationRole` | string |  |
| `teamMembers[].profileImageUrl` | string |  |
| `teamMembers[].timeZone` | string |  |

## Native endpoint

Through the native NeetoInvoice API, this operation is `GET /team_members` (base URL `https://{{credentials.workspaceSubdomain}}.neetoinvoice.com/api/external/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-team-members.md) for the provider-specific parameters and requirements.

