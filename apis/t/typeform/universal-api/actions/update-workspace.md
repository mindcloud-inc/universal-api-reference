# Typeform: Update Workspace



```
PUT https://connect.mindcloud.co/v1/universal/typeform/latest/actions/update-workspace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Typeform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/typeform/latest/actions/update-workspace" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspaceId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/typeform/latest/actions/update-workspace', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspaceId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `op` | string | no | Patch operation. |
| `path` | string | no | JSON pointer path for the patch. |
| `value` | string | no | Patch value. |
| `workspaceId` | string | yes | Typeform workspace identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": "string",
      "default": true,
      "forms": {
        "count": 1,
        "href": "string"
      },
      "id": "string",
      "members": [
        {
          "accountMemberId": "string",
          "email": "ava@example.com",
          "id": "string",
          "name": "Ava Chen",
          "permissions": [
            "string"
          ],
          "role": "string",
          "user": {
            "email": "ava@example.com",
            "id": "string",
            "name": "Ava Chen"
          }
        }
      ],
      "name": "Ava Chen",
      "self": {
        "href": "string"
      },
      "shared": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | string | Typeform account ID. |
| `default` | boolean | Whether this is the default workspace. |
| `forms` | object | Workspace forms metadata. |
| `forms.count` | number | Number of forms in workspace. |
| `forms.href` | string | Workspace forms API URL. |
| `id` | string | Workspace ID. |
| `members` | array<object> | Workspace members. |
| `members[].accountMemberId` | string | Account member ID. |
| `members[].email` | string | Member email. |
| `members[].id` | string | Workspace membership ID. |
| `members[].name` | string | Member display name. |
| `members[].permissions` | array<string> | Granted workspace permissions. |
| `members[].role` | string | Member role in workspace. |
| `members[].user` | object | Member user object. |
| `members[].user.email` | string | User email. |
| `members[].user.id` | string | User ID. |
| `members[].user.name` | string | User name. |
| `name` | string | Workspace name. |
| `self` | object | Workspace self link object. |
| `self.href` | string | Workspace self URL. |
| `shared` | boolean | Whether the workspace is shared. |

## Native endpoint

Through the native Typeform API, this operation is `PATCH /workspaces/:workspaceId` (base URL `https://api.typeform.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-workspace.md) for the provider-specific parameters and requirements.

