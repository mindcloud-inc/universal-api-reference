# 5pm: List All Users

Retrieves all users from 5pm.

```
GET https://connect.mindcloud.co/v1/universal/pm/latest/actions/list-all-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 5pm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pm/latest/actions/list-all-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pm/latest/actions/list-all-users?${params}`, {
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
      "count": 1,
      "items": [
        {
          "company": "string",
          "email": "ava@example.com",
          "firstName": "Ava",
          "id": "string",
          "lastName": "Chen",
          "title": "string"
        }
      ],
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number | Number of users in this page. |
| `items[].company` | string | User company name. |
| `items[].email` | string | User email address. |
| `items[].firstName` | string | User first name. |
| `items[].id` | string | User identifier. |
| `items[].lastName` | string | User last name. |
| `items[].title` | string | User title. |
| `total` | number | Total number of users available. |

## Native endpoint

Through the native 5pm API, this operation is `GET /service/get/users/getAll` (base URL `{{credentials.workspaceUrl}}/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-all-users.md) for the provider-specific parameters and requirements.

