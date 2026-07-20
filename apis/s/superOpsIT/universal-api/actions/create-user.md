# SuperOps IT: Create User



```
POST https://connect.mindcloud.co/v1/universal/superOpsIT/latest/actions/create-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SuperOps IT `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/superOpsIT/latest/actions/create-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "firstName": "Ava",
  "email": "ava@example.com",
  "roleId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/superOpsIT/latest/actions/create-user', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "firstName": "Ava",
    "email": "ava@example.com",
    "roleId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `firstName` | string | yes | The first name of the user. |
| `lastName` | string | no | The last name of the user. |
| `email` | string | yes | The email address used for login. |
| `contactNumber` | string | no | The contact number of the user. |
| `roleId` | string | yes | The application role ID to assign to the user. |
| `reportingManagerUserId` | string | no | The user ID of the reporting manager. |
| `departmentId` | string | no | The department ID for the user. |
| `siteId` | string | no | The site ID to associate to the user. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createUser": {
        "associations": [
          {
            "site": {
              "id": "string",
              "name": "Ava Chen"
            }
          }
        ],
        "contactNumber": "string",
        "email": "ava@example.com",
        "firstName": "Ava",
        "lastName": "Chen",
        "name": "Ava Chen",
        "roles": [
          {
            "name": "Ava Chen",
            "roleId": "string",
            "roleType": {
              "type": "string"
            }
          }
        ],
        "userId": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createUser.associations[].site.id` | string |  |
| `createUser.associations[].site.name` | string |  |
| `createUser.contactNumber` | string |  |
| `createUser.email` | string |  |
| `createUser.firstName` | string |  |
| `createUser.lastName` | string |  |
| `createUser.name` | string |  |
| `createUser.roles[].name` | string |  |
| `createUser.roles[].roleId` | string |  |
| `createUser.roles[].roleType.type` | string |  |
| `createUser.userId` | string |  |

## Native endpoint

Through the native SuperOps IT API, this operation is `POST /it` (base URL `https://api.superops.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-user.md) for the provider-specific parameters and requirements.

