# Zubie: Get Current User Profile

Retrieves the current user profile from Zubie.

```
GET https://connect.mindcloud.co/v1/universal/zubie/latest/actions/get-current-user-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zubie `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zubie/latest/actions/get-current-user-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zubie/latest/actions/get-current-user-profile?${params}`, {
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
      "account_key": "string",
      "account_role": "string",
      "email": "ava@example.com",
      "first_name": "Ava",
      "key": "string",
      "last_name": "Chen",
      "preferred_locale": "string",
      "updated": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account_key` | string |  |
| `account_role` | string |  |
| `email` | string |  |
| `first_name` | string |  |
| `key` | string |  |
| `last_name` | string |  |
| `preferred_locale` | string |  |
| `updated` | string |  |

## Native endpoint

Through the native Zubie API, this operation is `GET /user` (base URL `https://api.zubiecar.com/api/v2/zinc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-user-profile.md) for the provider-specific parameters and requirements.

