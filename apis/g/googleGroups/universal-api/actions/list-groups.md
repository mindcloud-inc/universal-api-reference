# Google Groups: List Groups

Retrieves groups from Google Groups for a domain or user.

```
GET https://connect.mindcloud.co/v1/universal/googleGroups/latest/actions/list-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Groups `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleGroups/latest/actions/list-groups?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleGroups/latest/actions/list-groups?${params}`, {
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
| `query` | string | no | Search expression for Google Groups. |
| `maxResults` | number | no | Maximum number of groups to return per page. Default: `100`. |
| `orderBy` | string | no | Field to sort by. One of: `0`. |
| `sortOrder` | string | no | Sort direction when orderBy is provided. One of: `0`, `1`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `domain` | string | no | Limit results to a single domain instead of the full customer. |
| `userKey` | string | no | List only groups that the specified user belongs to. |
| `pageToken` | string | no | Token for the next page of results. |

## Response

```json
{
  "success": true,
  "data": [
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
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `adminCreated` | boolean | Whether the group was created by an administrator. |
| `description` | string | Group description text. |
| `directMembersCount` | string | Count of direct members returned by Google. |
| `email` | string | Primary email address of the group. |
| `etag` | string | Entity tag for the group resource. |
| `id` | string | Unique Google group ID. |
| `kind` | string | Google resource type for the group row. |
| `name` | string | Display name of the group. |
| `nonEditableAliases` | array<string> | Aliases Google marks as non-editable for the group. |

## Native endpoint

Through the native Google Groups API, this operation is `GET https://admin.googleapis.com/admin/directory/v1/groups` (base URL `https://groups.google.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-groups.md) for the provider-specific parameters and requirements.

