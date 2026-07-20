# Paycove: Get Current User

Retrieves the current user from Paycove.

```
GET https://connect.mindcloud.co/v1/universal/paycove/latest/actions/get-current-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paycove `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/paycove/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/paycove/latest/actions/get-current-user?${params}`, {
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
      "account": {
        "uniqueId": "string"
      },
      "accountId": 1,
      "createdAt": "string",
      "deletedAt": {},
      "email": "ava@example.com",
      "id": 1,
      "isAdmin": 1,
      "logins": 1,
      "name": "Ava Chen",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account.uniqueId` | string |  |
| `accountId` | number |  |
| `createdAt` | string |  |
| `deletedAt` | object |  |
| `email` | string |  |
| `id` | number |  |
| `isAdmin` | number |  |
| `logins` | number |  |
| `name` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Paycove API, this operation is `GET user` (base URL `https://paycove.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-user.md) for the provider-specific parameters and requirements.

