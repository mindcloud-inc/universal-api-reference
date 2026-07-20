# Kite Suite: Add new role in workspace



```
POST https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/add-new-role-in-workspace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kite Suite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/add-new-role-in-workspace" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "body": {},
  "roleName": "Ava Chen",
  "workspace": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/add-new-role-in-workspace', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "body": {},
    "roleName": "Ava Chen",
    "workspace": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `body` | object | yes | Request body |
| `roleName` | string | yes |  |
| `workspace` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "createAt": "string",
      "permissions": {},
      "roleName": "Ava Chen",
      "tenant": "string",
      "updatedAt": "string",
      "workspace": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string | The auto-generated id of the role. |
| `createAt` | string | Creation time of role. |
| `permissions` | object | Permissions of role. |
| `roleName` | string | Name of role |
| `tenant` | string | Tenant ID of role or null for default role. |
| `updatedAt` | string | Updated time of role.* |
| `workspace` | string | Workspace Id of the Role or null for default role. |

## Native endpoint

Through the native Kite Suite API, this operation is `POST /api/v1/workspace-role` (base URL `https://api.kitesuite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-new-role-in-workspace.md) for the provider-specific parameters and requirements.

