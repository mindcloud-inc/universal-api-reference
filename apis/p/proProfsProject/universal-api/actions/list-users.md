# ProProfs Project: List Users

Retrieves a list of users from ProProfs Project.

```
GET https://connect.mindcloud.co/v1/universal/proProfsProject/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProProfs Project `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/proProfsProject/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/proProfsProject/latest/actions/list-users?${params}`, {
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
      "data": [
        {
          "avatar": "string",
          "createdBy": "string",
          "dateCreated": "string",
          "email": "ava@example.com",
          "lastLogin": "string",
          "registered": true,
          "updatedBy": "string",
          "userId": "string",
          "userName": "Ava Chen"
        }
      ],
      "paging": {
        "limit": 1,
        "offset": 1,
        "totalRecords": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].avatar` | string |  |
| `data[].createdBy` | string |  |
| `data[].dateCreated` | string |  |
| `data[].email` | string |  |
| `data[].lastLogin` | string |  |
| `data[].registered` | boolean |  |
| `data[].updatedBy` | string |  |
| `data[].userId` | string |  |
| `data[].userName` | string |  |
| `paging.limit` | number |  |
| `paging.offset` | number |  |
| `paging.totalRecords` | number |  |

## Native endpoint

Through the native ProProfs Project API, this operation is `GET /users` (base URL `https://api.projectbubble.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

