# SuperOps IT: List Users



```
GET https://connect.mindcloud.co/v1/universal/superOpsIT/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SuperOps IT `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/superOpsIT/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/superOpsIT/latest/actions/list-users?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "getUserList": {
        "listInfo": {
          "page": 1,
          "pageSize": 1,
          "totalCount": 1
        },
        "userList": [
          {
            "associations": [
              {
                "site": {
                  "id": "string",
                  "name": "Ava Chen"
                }
              }
            ],
            "contactNumber": "string",
            "department": {
              "name": "Ava Chen"
            },
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
        ]
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `getUserList.listInfo.page` | number |  |
| `getUserList.listInfo.pageSize` | number |  |
| `getUserList.listInfo.totalCount` | number |  |
| `getUserList.userList[].associations[].site.id` | string |  |
| `getUserList.userList[].associations[].site.name` | string |  |
| `getUserList.userList[].contactNumber` | string |  |
| `getUserList.userList[].department.name` | string |  |
| `getUserList.userList[].email` | string |  |
| `getUserList.userList[].firstName` | string |  |
| `getUserList.userList[].lastName` | string |  |
| `getUserList.userList[].name` | string |  |
| `getUserList.userList[].roles[].name` | string |  |
| `getUserList.userList[].roles[].roleId` | string |  |
| `getUserList.userList[].roles[].roleType.type` | string |  |
| `getUserList.userList[].userId` | string |  |

## Native endpoint

Through the native SuperOps IT API, this operation is `POST /it` (base URL `https://api.superops.ai`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

