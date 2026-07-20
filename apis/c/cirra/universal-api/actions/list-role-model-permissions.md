# Cirra: List Role Model Permissions



```
GET https://connect.mindcloud.co/v1/universal/cirra/latest/actions/list-role-model-permissions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cirra `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cirra/latest/actions/list-role-model-permissions?connectionId=$CONNECTION_ID&limit=25&offset=0&roleId=string&appId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "roleId": "string",
  "appId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cirra/latest/actions/list-role-model-permissions?${params}`, {
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
| `roleId` | list | yes |  |
| `appId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "app": {
        "icon": "string",
        "id": "string",
        "name": "Ava Chen",
        "slug": "string"
      },
      "appPermissions": {
        "allowCreate": true,
        "allowDelete": true,
        "allowRead": true,
        "allowUpdate": true,
        "inheritsGlobal": true
      },
      "globalPermissions": {
        "allowCreate": true,
        "allowDelete": true,
        "allowRead": true,
        "allowUpdate": true
      },
      "models": [
        {}
      ],
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
| `app.icon` | string |  |
| `app.id` | string |  |
| `app.name` | string |  |
| `app.slug` | string |  |
| `appPermissions.allowCreate` | boolean |  |
| `appPermissions.allowDelete` | boolean |  |
| `appPermissions.allowRead` | boolean |  |
| `appPermissions.allowUpdate` | boolean |  |
| `appPermissions.inheritsGlobal` | boolean |  |
| `globalPermissions.allowCreate` | boolean |  |
| `globalPermissions.allowDelete` | boolean |  |
| `globalPermissions.allowRead` | boolean |  |
| `globalPermissions.allowUpdate` | boolean |  |
| `models` | array<object> |  |
| `role.companyId` | string |  |
| `role.description` | string |  |
| `role.id` | string |  |
| `role.isBuiltIn` | boolean |  |
| `role.name` | string |  |

## Native endpoint

Through the native Cirra API, this operation is `GET /v1/cirra/roles/:roleId/permissions/apps/:appId/models` (base URL `http://api-public:9801`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-role-model-permissions.md) for the provider-specific parameters and requirements.

