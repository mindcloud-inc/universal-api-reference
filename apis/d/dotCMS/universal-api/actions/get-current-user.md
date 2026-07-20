# DotCMS: Get Current User

Retrieves the authenticated user from DotCMS.

```
GET https://connect.mindcloud.co/v1/universal/dotCMS/latest/actions/get-current-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DotCMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dotCMS/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dotCMS/latest/actions/get-current-user?${params}`, {
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
      "admin": true,
      "email": "ava@example.com",
      "givenName": "Ava Chen",
      "loginAs": true,
      "roleId": "string",
      "surname": "Ava Chen",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `admin` | boolean | Whether the current user has administrative access. |
| `email` | string | Email address of the current DotCMS user. |
| `givenName` | string | Given name of the current DotCMS user. |
| `loginAs` | boolean | Whether the current session is in login-as mode. |
| `roleId` | string | Primary role identifier for the current DotCMS user. |
| `surname` | string | Surname of the current DotCMS user. |
| `userId` | string | DotCMS user identifier. |

## Native endpoint

Through the native DotCMS API, this operation is `GET /api/v1/users/current` (base URL `https://demo.dotcms.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-user.md) for the provider-specific parameters and requirements.

