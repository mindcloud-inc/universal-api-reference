# ForceManager: Read Users

Retrieves users from your ForceManager account.

```
GET https://connect.mindcloud.co/v1/universal/forceManager/latest/actions/read-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ForceManager `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/forceManager/latest/actions/read-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/forceManager/latest/actions/read-users?${params}`, {
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
      "branchId": 1,
      "branchName": "Ava Chen",
      "email": "ava@example.com",
      "enabled": true,
      "firstName": "Ava",
      "id": 1,
      "lastName": "Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `branchId` | number | ID of the branch the user is assigned to. |
| `branchName` | string | Name of the branch. |
| `email` | string | Email of the user. |
| `enabled` | boolean | Whether the user is enabled. |
| `firstName` | string | User's first name. |
| `id` | number | Unique identifier for the user. |
| `lastName` | string | User's last name. |

## Native endpoint

Through the native ForceManager API, this operation is `GET /users`. The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/read-users.md) for the provider-specific parameters and requirements.

