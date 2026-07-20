# retailCRM: List Users

Retrieves users from retailCRM.

```
GET https://connect.mindcloud.co/v1/universal/retailCRM/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a retailCRM `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/retailCRM/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/retailCRM/latest/actions/list-users?${params}`, {
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
      "active": true,
      "createdAt": "string",
      "email": "ava@example.com",
      "firstName": "Ava",
      "groups": [
        {
          "code": "string",
          "id": 1,
          "name": "Ava Chen"
        }
      ],
      "id": 1,
      "isAdmin": true,
      "isManager": true,
      "lastName": "Chen",
      "online": true,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `createdAt` | string |  |
| `email` | string |  |
| `firstName` | string |  |
| `groups[].code` | string |  |
| `groups[].id` | number |  |
| `groups[].name` | string |  |
| `id` | number |  |
| `isAdmin` | boolean |  |
| `isManager` | boolean |  |
| `lastName` | string |  |
| `online` | boolean |  |
| `status` | string |  |

## Native endpoint

Through the native retailCRM API, this operation is `GET /users` (base URL `{{credentials.accountUrl}}/api/v5`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

