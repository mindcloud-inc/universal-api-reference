# Yay.com: List Reseller Users

Retrieves reseller users from Yay.com.

```
GET https://connect.mindcloud.co/v1/universal/yaycom/latest/actions/list-reseller-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Yay.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yaycom/latest/actions/list-reseller-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/yaycom/latest/actions/list-reseller-users?${params}`, {
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
      "contactFirstName": "Ava",
      "contactLastName": "Chen",
      "createdOn": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "isStoreUser": true,
      "loginHistory": [
        {}
      ],
      "name": "Ava Chen",
      "objectAccess": [
        {}
      ],
      "roleId": 1,
      "sendResetLink": true,
      "statusId": 1,
      "timezone": "string",
      "userEmail": "ava@example.com",
      "userName": "Ava Chen",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contactFirstName` | string | User first name when present. |
| `contactLastName` | string | User last name when present. |
| `createdOn` | date | Creation timestamp. |
| `email` | string | Email returned by Yay when present. |
| `isStoreUser` | boolean | Whether the reseller user is also a store user. |
| `loginHistory` | array<object> | Recent login events returned by Yay. |
| `name` | string | Display name returned by Yay. |
| `objectAccess` | array<object> | Object access entries returned by Yay. |
| `roleId` | number | Reseller user role identifier. |
| `sendResetLink` | boolean | Whether a reset link should be sent. |
| `statusId` | number | Yay status identifier. |
| `timezone` | string | User timezone setting. |
| `userEmail` | string | User email when present. |
| `userName` | string | Username used for the reseller user. |
| `uuid` | string | Unique reseller user identifier. |

## Native endpoint

Through the native Yay.com API, this operation is `GET /account/reseller-user` (base URL `https://api.yay.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-reseller-users.md) for the provider-specific parameters and requirements.

