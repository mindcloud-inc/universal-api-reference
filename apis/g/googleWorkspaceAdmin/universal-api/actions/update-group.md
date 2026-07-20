# Google Workspace Admin: Update Group

Updates an existing group in Google Workspace Admin.

```
PUT https://connect.mindcloud.co/v1/universal/googleWorkspaceAdmin/latest/actions/update-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Workspace Admin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/googleWorkspaceAdmin/latest/actions/update-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "groupKey": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleWorkspaceAdmin/latest/actions/update-group', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "groupKey": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `description` | string | no | Optional description for the group. |
| `email` | string | no | Primary email address for the group. |
| `groupKey` | string | yes | Group email address, alias, or unique ID. |
| `name` | string | no | Display name for the group. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "adminCreated": true,
      "description": "string",
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
| `adminCreated` | boolean |  |
| `description` | string |  |
| `email` | string |  |
| `etag` | string |  |
| `id` | string |  |
| `kind` | string |  |
| `name` | string |  |
| `nonEditableAliases` | array<string> |  |

## Native endpoint

Through the native Google Workspace Admin API, this operation is `PUT /admin/directory/v1/groups/:groupKey` (base URL `https://admin.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-group.md) for the provider-specific parameters and requirements.

