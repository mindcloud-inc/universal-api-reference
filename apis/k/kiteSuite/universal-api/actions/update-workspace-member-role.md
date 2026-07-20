# KiteSuite: Update Workspace Member Role

Updates a workspace member role in KiteSuite.

```
PUT https://connect.mindcloud.co/v1/universal/kiteSuite/latest/actions/update-workspace-member-role
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KiteSuite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/kiteSuite/latest/actions/update-workspace-member-role" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "roleID": "e.g. 69cfacd46d907abc77fcc550"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kiteSuite/latest/actions/update-workspace-member-role', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "roleID": "e.g. 69cfacd46d907abc77fcc550"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Runtime expects the user ID for the workspace member. |
| `roleID` | string | yes | Workspace role ID to assign. Example: `e.g. 69cfacd46d907abc77fcc550`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "email": "ava@example.com",
      "fullName": "Ava Chen",
      "status": "string",
      "workspaces": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string |  |
| `email` | string |  |
| `fullName` | string |  |
| `status` | string |  |
| `workspaces` | array<object> |  |

## Native endpoint

Through the native KiteSuite API, this operation is `PATCH /api/v1/workspace/member/:id` (base URL `https://api.kitesuite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-workspace-member-role.md) for the provider-specific parameters and requirements.

