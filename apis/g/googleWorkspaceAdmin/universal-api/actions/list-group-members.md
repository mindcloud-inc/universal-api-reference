# Google Workspace Admin: List Group Members

Retrieves members from a Google Workspace Admin group.

```
GET https://connect.mindcloud.co/v1/universal/googleWorkspaceAdmin/latest/actions/list-group-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Workspace Admin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleWorkspaceAdmin/latest/actions/list-group-members?connectionId=$CONNECTION_ID&groupKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "groupKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleWorkspaceAdmin/latest/actions/list-group-members?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `groupKey` | string | yes | Group email address, alias, or unique ID. |
| `includeDerivedMembership` | boolean | no | Include indirect memberships in the result. |
| `maxResults` | number | no | Maximum number of members to return (up to 200). |
| `pageToken` | string | no | Pagination token from a previous members list response. |
| `roles` | string | no | Filter members by role: OWNER, MANAGER, or MEMBER. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "etag": "string",
      "kind": "string",
      "members": [
        {
          "email": "ava@example.com",
          "etag": "string",
          "id": "string",
          "kind": "string",
          "role": "string",
          "status": "string",
          "type": "string"
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
| `etag` | string |  |
| `kind` | string |  |
| `members[].email` | string |  |
| `members[].etag` | string |  |
| `members[].id` | string |  |
| `members[].kind` | string |  |
| `members[].role` | string |  |
| `members[].status` | string |  |
| `members[].type` | string |  |

## Native endpoint

Through the native Google Workspace Admin API, this operation is `GET /admin/directory/v1/groups/:groupKey/members` (base URL `https://admin.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-group-members.md) for the provider-specific parameters and requirements.

