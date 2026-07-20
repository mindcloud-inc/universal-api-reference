# Google Workspace Admin: List Groups

Retrieves groups from Google Workspace Admin.

```
GET https://connect.mindcloud.co/v1/universal/googleWorkspaceAdmin/latest/actions/list-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Workspace Admin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleWorkspaceAdmin/latest/actions/list-groups?connectionId=$CONNECTION_ID&customer=my_customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customer": "my_customer"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleWorkspaceAdmin/latest/actions/list-groups?${params}`, {
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
| `customer` | string | yes | Google customer identifier. Use my_customer for current tenant. Default: `my_customer`. |
| `domain` | string | no | Optional domain to limit listed groups to one domain. |
| `orderBy` | string | no | Field to sort groups by, for example email. |
| `pageToken` | string | no | Pagination token from a previous groups list response. |
| `query` | string | no | Search query for matching groups. |
| `sortOrder` | string | no | Sort direction for the results. |
| `userKey` | string | no | Only list groups that include this user as a member. |
| `maxResults` | number | no | Maximum number of users to return per page. Default: `100`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "etag": "string",
      "groups": [
        {
          "adminCreated": true,
          "description": "string",
          "directMembersCount": "string",
          "email": "ava@example.com",
          "etag": "string",
          "id": "string",
          "kind": "string",
          "name": "Ava Chen",
          "nonEditableAliases": [
            "string"
          ]
        }
      ],
      "kind": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `etag` | string |  |
| `groups[].adminCreated` | boolean |  |
| `groups[].description` | string |  |
| `groups[].directMembersCount` | string |  |
| `groups[].email` | string |  |
| `groups[].etag` | string |  |
| `groups[].id` | string |  |
| `groups[].kind` | string |  |
| `groups[].name` | string |  |
| `groups[].nonEditableAliases[]` | string |  |
| `kind` | string |  |

## Native endpoint

Through the native Google Workspace Admin API, this operation is `GET /admin/directory/v1/groups` (base URL `https://admin.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-groups.md) for the provider-specific parameters and requirements.

