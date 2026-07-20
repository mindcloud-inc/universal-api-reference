# Yampi: Get Authenticated User

Retrieves the authenticated user from Yampi.

```
GET https://connect.mindcloud.co/v1/universal/yampi/latest/actions/get-authenticated-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Yampi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yampi/latest/actions/get-authenticated-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/yampi/latest/actions/get-authenticated-user?${params}`, {
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
      "email": "ava@example.com",
      "id": 1,
      "merchantOwner": true,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean | Whether the authenticated user is active. |
| `email` | string | Authenticated Yampi user email address. |
| `id` | number | Authenticated Yampi user ID. |
| `merchantOwner` | boolean | Whether the authenticated user owns a merchant account. |
| `name` | string | Authenticated Yampi user name. |

## Native endpoint

Through the native Yampi API, this operation is `POST /auth/me` (base URL `https://api.dooki.com.br/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-authenticated-user.md) for the provider-specific parameters and requirements.

