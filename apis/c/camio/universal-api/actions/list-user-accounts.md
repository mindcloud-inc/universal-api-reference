# Camio: List User Accounts

Retrieves user accounts from Camio.

```
GET https://connect.mindcloud.co/v1/universal/camio/latest/actions/list-user-accounts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Camio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/camio/latest/actions/list-user-accounts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/camio/latest/actions/list-user-accounts?${params}`, {
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
      "ipAddress": "string",
      "userEmail": "ava@example.com",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ipAddress` | string | The caller IP address returned by Camio. |
| `userEmail` | string | The email on the account. |
| `userId` | string | The Camio user id. |

## Native endpoint

Through the native Camio API, this operation is `GET /users/:user/accounts` (base URL `https://camio.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-user-accounts.md) for the provider-specific parameters and requirements.

