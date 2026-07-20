# Cirra: Set Role App Permissions



```
PUT https://connect.mindcloud.co/v1/universal/cirra/latest/actions/set-role-app-permissions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cirra `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/cirra/latest/actions/set-role-app-permissions" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "roleId": "string",
  "appId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cirra/latest/actions/set-role-app-permissions', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "roleId": "string",
    "appId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `roleId` | list | yes |  |
| `appId` | list | yes |  |
| `allowRead` | boolean | no | Optional CRUD override flag. Omit unchanged operations. Default: `true`. |
| `allowCreate` | boolean | no | Optional CRUD override flag. Omit unchanged operations. Default: `true`. |
| `allowUpdate` | boolean | no | Optional CRUD override flag. Omit unchanged operations. Default: `true`. |
| `allowDelete` | boolean | no | Optional CRUD override flag. Omit unchanged operations. Default: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "appId": "string",
      "permissions": {
        "allowCreate": true,
        "allowDelete": true,
        "allowRead": true,
        "allowUpdate": true,
        "inheritsGlobal": true
      },
      "role": {
        "companyId": "string",
        "description": "string",
        "id": "string",
        "isBuiltIn": true,
        "name": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `appId` | string |  |
| `permissions.allowCreate` | boolean |  |
| `permissions.allowDelete` | boolean |  |
| `permissions.allowRead` | boolean |  |
| `permissions.allowUpdate` | boolean |  |
| `permissions.inheritsGlobal` | boolean |  |
| `role.companyId` | string |  |
| `role.description` | string |  |
| `role.id` | string |  |
| `role.isBuiltIn` | boolean |  |
| `role.name` | string |  |

## Native endpoint

Through the native Cirra API, this operation is `PUT /v1/cirra/roles/:roleId/permissions/apps/:appId` (base URL `http://api-public:9801`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-role-app-permissions.md) for the provider-specific parameters and requirements.

