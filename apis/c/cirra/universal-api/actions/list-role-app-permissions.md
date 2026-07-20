# Cirra: List Role App Permissions



```
GET https://connect.mindcloud.co/v1/universal/cirra/latest/actions/list-role-app-permissions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cirra `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cirra/latest/actions/list-role-app-permissions?connectionId=$CONNECTION_ID&limit=25&offset=0&roleId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "roleId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cirra/latest/actions/list-role-app-permissions?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "apps": [
        {}
      ],
      "globalPermissions": {
        "allowCreate": true,
        "allowDelete": true,
        "allowRead": true,
        "allowUpdate": true
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
| `apps` | array<object> |  |
| `globalPermissions.allowCreate` | boolean |  |
| `globalPermissions.allowDelete` | boolean |  |
| `globalPermissions.allowRead` | boolean |  |
| `globalPermissions.allowUpdate` | boolean |  |
| `role.companyId` | string |  |
| `role.description` | string |  |
| `role.id` | string |  |
| `role.isBuiltIn` | boolean |  |
| `role.name` | string |  |

## Native endpoint

Through the native Cirra API, this operation is `GET /v1/cirra/roles/:roleId/permissions/apps` (base URL `http://api-public:9801`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-role-app-permissions.md) for the provider-specific parameters and requirements.

