# Kite Suite: Add New Project Roles



```
POST https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/add-new-project-roles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kite Suite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/add-new-project-roles" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "body": {},
  "roleName": "Ava Chen",
  "project": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/add-new-project-roles', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "body": {},
    "roleName": "Ava Chen",
    "project": "string"
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
| `project` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "createAt": "string",
      "permissions": {},
      "project": "string",
      "roleName": "Ava Chen",
      "tenant": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string | The auto-generated id of the project role. |
| `createAt` | string | Creation time of project role. |
| `permissions` | object | Permissions of project role. |
| `project` | string | project Id of the project Role or null for default project role. |
| `roleName` | string | Name of project role |
| `tenant` | string | Tenant ID of role or null for default project role. |
| `updatedAt` | string | Updated time of project role.* |

## Native endpoint

Through the native Kite Suite API, this operation is `POST /api/v1/project-role` (base URL `https://api.kitesuite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-new-project-roles.md) for the provider-specific parameters and requirements.

