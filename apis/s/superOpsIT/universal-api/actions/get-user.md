# SuperOps IT: Get User



```
GET https://connect.mindcloud.co/v1/universal/superOpsIT/latest/actions/get-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SuperOps IT `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/superOpsIT/latest/actions/get-user?connectionId=$CONNECTION_ID&userId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/superOpsIT/latest/actions/get-user?${params}`, {
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
| `userId` | string | yes | The ID of the user to fetch. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "getUser": {
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
| `getUser.associations[].site.id` | string |  |
| `getUser.associations[].site.name` | string |  |
| `getUser.contactNumber` | string |  |
| `getUser.email` | string |  |
| `getUser.firstName` | string |  |
| `getUser.lastName` | string |  |
| `getUser.name` | string |  |
| `getUser.roles[].name` | string |  |
| `getUser.roles[].roleId` | string |  |
| `getUser.roles[].roleType.type` | string |  |
| `getUser.userId` | string |  |

## Native endpoint

Through the native SuperOps IT API, this operation is `POST /it` (base URL `https://api.superops.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user.md) for the provider-specific parameters and requirements.

