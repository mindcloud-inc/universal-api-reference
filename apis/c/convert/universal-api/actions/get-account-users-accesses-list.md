# Convert: List Account User Accesses

Retrieves user access entries for a Convert account.

```
GET https://connect.mindcloud.co/v1/universal/convert/latest/actions/get-account-users-accesses-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Convert `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/convert/latest/actions/get-account-users-accesses-list?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/convert/latest/actions/get-account-users-accesses-list?${params}`, {
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
      "accesses": [
        {
          "api_access": true,
          "role": "string",
          "status": "string"
        }
      ],
      "email": "ava@example.com",
      "first_name": "Ava",
      "last_name": "Chen",
      "user_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accesses[].api_access` | boolean |  |
| `accesses[].role` | string |  |
| `accesses[].status` | string |  |
| `email` | string |  |
| `first_name` | string |  |
| `last_name` | string |  |
| `user_id` | string |  |

## Native endpoint

Through the native Convert API, this operation is `GET /accounts/:account_id/users-accesses` (base URL `https://api.convert.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account-users-accesses-list.md) for the provider-specific parameters and requirements.

