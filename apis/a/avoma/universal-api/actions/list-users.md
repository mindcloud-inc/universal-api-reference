# Avoma: List Users

Retrieves users from Avoma.

```
GET https://connect.mindcloud.co/v1/universal/avoma/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Avoma `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/avoma/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/avoma/latest/actions/list-users?${params}`, {
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
      "position": "string",
      "role": {
        "description": "string",
        "displayName": "Ava Chen",
        "name": "Ava Chen",
        "roleType": "string",
        "uuid": "string"
      },
      "status": "string",
      "user": {
        "email": "ava@example.com",
        "firstName": "Ava",
        "isActive": true,
        "jobFunction": "string",
        "lastName": "Chen",
        "position": "string"
      },
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `position` | string |  |
| `role.description` | string |  |
| `role.displayName` | string |  |
| `role.name` | string |  |
| `role.roleType` | string |  |
| `role.uuid` | string |  |
| `status` | string |  |
| `user.email` | string |  |
| `user.firstName` | string |  |
| `user.isActive` | boolean |  |
| `user.jobFunction` | string |  |
| `user.lastName` | string |  |
| `user.position` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native Avoma API, this operation is `GET /v1/users/` (base URL `https://api.avoma.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

