# Mendix: Get Project Role

Retrieves a project role from Mendix.

```
GET https://connect.mindcloud.co/v1/universal/mendix/latest/actions/get-project-role
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mendix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mendix/latest/actions/get-project-role?connectionId=$CONNECTION_ID&roleId=fdea56de-3c79-48d9-93ff-61cbc736426c" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "roleId": "fdea56de-3c79-48d9-93ff-61cbc736426c"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mendix/latest/actions/get-project-role?${params}`, {
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
| `roleId` | string | yes | The unique identifier of a project role. Example: `fdea56de-3c79-48d9-93ff-61cbc736426c`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account": {
        "accountId": "string",
        "accountName": "Ava Chen"
      },
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
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account.accountId` | string | Unique identifier of the account. |
| `account.accountName` | string | Name of the account. |
| `environmentPermissions[].accessType` | string | Access type for the environment permission set. |
| `environmentPermissions[].environmentType` | string | Environment type covered by the permission set. |
| `environmentPermissions[].hasApiRights` | boolean | Indicates whether the role has API rights. |
| `environmentPermissions[].hasBackupAccess` | boolean | Indicates whether the role has backup access. |
| `environmentPermissions[].hasManageRights` | boolean | Indicates whether the role has manage rights. |
| `environmentPermissions[].hasMonitoringAccess` | boolean | Indicates whether the role has monitoring access. |
| `environmentPermissions[].hasTransportRights` | boolean | Indicates whether the role has transport rights. |
| `hasCloudAccess` | boolean | Indicates whether the role has cloud access. |
| `hasInvitationRights` | boolean | Indicates whether the role can invite users. |
| `hasRepositoryAccess` | boolean | Indicates whether the role has repository access. |
| `hasStoryAccess` | boolean | Indicates whether the role has story access. |
| `isAdministrator` | boolean | Indicates whether the role is an administrator role. |
| `roleDescription` | string | Description of the project role. |
| `roleId` | string | Unique identifier of the project role. |
| `roleName` | string | Name of the project role. |

## Native endpoint

Through the native Mendix API, this operation is `GET /roles/:roleId` (base URL `https://projects-api.home.mendix.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project-role.md) for the provider-specific parameters and requirements.

