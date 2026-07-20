# Kite Suite: Get workspace roles by tenant ID



```
GET https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/get-workspace-roles-by-tenant-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kite Suite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/get-workspace-roles-by-tenant-id?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/get-workspace-roles-by-tenant-id?${params}`, {
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
| `id` | string | no |  |

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

Through the native Kite Suite API, this operation is `GET /api/v1/workspace-role/tenant/:id` (base URL `https://api.kitesuite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-workspace-roles-by-tenant-id.md) for the provider-specific parameters and requirements.

