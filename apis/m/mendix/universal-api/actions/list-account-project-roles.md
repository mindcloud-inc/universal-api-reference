# Mendix: List Account Project Roles

Retrieves project roles for an account in Mendix.

```
GET https://connect.mindcloud.co/v1/universal/mendix/latest/actions/list-account-project-roles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mendix `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mendix/latest/actions/list-account-project-roles?connectionId=$CONNECTION_ID&limit=25&offset=0&accountId=b8f3f8f9-245e-4c9e-b0a1-69d2e1f2aa10" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "accountId": "b8f3f8f9-245e-4c9e-b0a1-69d2e1f2aa10"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mendix/latest/actions/list-account-project-roles?${params}`, {
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
| `accountId` | string | yes | The unique identifier of the account or company. Example: `b8f3f8f9-245e-4c9e-b0a1-69d2e1f2aa10`. |
| `changedSince` | date | no | Only return roles created or changed since this ISO 8601 date and time. Example: `2024-08-20T14:15:22Z`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
        {
          "environmentPermissions": [
            {
              "accessType": "string",
              "environmentType": "string",
              "hasApiRights": true,
              "hasBackupAccess": true,
              "hasManageRights": true,
              "hasMonitoringAccess": true,
              "hasTransportRights": true
            }
          ],
          "hasCloudAccess": true,
          "hasInvitationRights": true,
          "hasRepositoryAccess": true,
          "hasStoryAccess": true,
          "isAdministrator": true,
          "roleDescription": "string",
          "roleId": "string",
          "roleName": "Ava Chen"
        }
      ],
      "page": {
        "elements": 1,
        "offset": 1,
        "totalElements": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items[].environmentPermissions[].accessType` | string | Access type for the environment permission set. |
| `items[].environmentPermissions[].environmentType` | string | Environment type covered by the permission set. |
| `items[].environmentPermissions[].hasApiRights` | boolean | Indicates whether the role has API rights. |
| `items[].environmentPermissions[].hasBackupAccess` | boolean | Indicates whether the role has backup access. |
| `items[].environmentPermissions[].hasManageRights` | boolean | Indicates whether the role has manage rights. |
| `items[].environmentPermissions[].hasMonitoringAccess` | boolean | Indicates whether the role has monitoring access. |
| `items[].environmentPermissions[].hasTransportRights` | boolean | Indicates whether the role has transport rights. |
| `items[].hasCloudAccess` | boolean | Indicates whether the role has cloud access. |
| `items[].hasInvitationRights` | boolean | Indicates whether the role can invite users. |
| `items[].hasRepositoryAccess` | boolean | Indicates whether the role has repository access. |
| `items[].hasStoryAccess` | boolean | Indicates whether the role has story access. |
| `items[].isAdministrator` | boolean | Indicates whether the role is an administrator role. |
| `items[].roleDescription` | string | Description of the project role. |
| `items[].roleId` | string | Unique identifier of the project role. |
| `items[].roleName` | string | Name of the project role. |
| `page.elements` | number | Number of elements returned. |
| `page.offset` | number | Pagination offset. |
| `page.totalElements` | number | Total number of matching project roles. |

## Native endpoint

Through the native Mendix API, this operation is `GET /accounts/:accountId/roles` (base URL `https://projects-api.home.mendix.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-account-project-roles.md) for the provider-specific parameters and requirements.

