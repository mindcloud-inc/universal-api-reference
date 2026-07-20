# OpnForm: Update Workspace User Role

Updates a user's role in an OpnForm workspace.

```
PUT https://connect.mindcloud.co/v1/universal/opnForm/latest/actions/update-workspace-user-role
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpnForm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/opnForm/latest/actions/update-workspace-user-role" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspaceId": 1,
  "userId": 1,
  "role": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/opnForm/latest/actions/update-workspace-user-role', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspaceId": 1,
    "userId": 1,
    "role": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspaceId` | number | yes |  |
| `userId` | number | yes |  |
| `role` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `type` | string |  |

## Native endpoint

Through the native OpnForm API, this operation is `PUT /open/workspaces/:workspaceId/users/:userId/update-role` (base URL `https://api.opnform.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-workspace-user-role.md) for the provider-specific parameters and requirements.

