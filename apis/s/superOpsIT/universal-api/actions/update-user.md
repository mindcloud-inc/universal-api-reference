# SuperOps IT: Update User



```
PUT https://connect.mindcloud.co/v1/universal/superOpsIT/latest/actions/update-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SuperOps IT `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/superOpsIT/latest/actions/update-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "userId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/superOpsIT/latest/actions/update-user', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "userId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `userId` | string | yes | The ID of the user to update. |
| `firstName` | string | no | The first name of the user. |
| `lastName` | string | no | The last name of the user. |
| `email` | string | no | The email address used for login. |
| `contactNumber` | string | no | The contact number of the user. |
| `roleId` | string | no | The application role ID to assign to the user. |
| `reportingManagerUserId` | string | no | The user ID of the reporting manager. |
| `departmentId` | string | no | The department ID for the user. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "updateUser": {
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
| `updateUser.associations[].site.id` | string |  |
| `updateUser.associations[].site.name` | string |  |
| `updateUser.contactNumber` | string |  |
| `updateUser.email` | string |  |
| `updateUser.firstName` | string |  |
| `updateUser.lastName` | string |  |
| `updateUser.name` | string |  |
| `updateUser.roles[].name` | string |  |
| `updateUser.roles[].roleId` | string |  |
| `updateUser.roles[].roleType.type` | string |  |
| `updateUser.userId` | string |  |

## Native endpoint

Through the native SuperOps IT API, this operation is `POST /it` (base URL `https://api.superops.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-user.md) for the provider-specific parameters and requirements.

