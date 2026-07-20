# Callbell: Get Auth Me

Retrieves current authenticated user details from Callbell.

```
GET https://connect.mindcloud.co/v1/universal/callbell/latest/actions/get-auth-me
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Callbell `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/callbell/latest/actions/get-auth-me?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/callbell/latest/actions/get-auth-me?${params}`, {
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
      "api_key": "string",
      "status": "string",
      "user_email": "ava@example.com",
      "user_name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `api_key` | string |  |
| `status` | string |  |
| `user_email` | string |  |
| `user_name` | string |  |

## Native endpoint

Through the native Callbell API, this operation is `GET /auth/me` (base URL `https://api.callbell.eu/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-auth-me.md) for the provider-specific parameters and requirements.

