# Pachca: Get token info



```
GET https://connect.mindcloud.co/v1/universal/pachca/latest/actions/get-token-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pachca `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pachca/latest/actions/get-token-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pachca/latest/actions/get-token-info?${params}`, {
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
      "created_at": "2026-05-07T12:00:00.000Z",
      "expires_in": 1,
      "id": 1,
      "last_used_at": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "revoked_at": "2026-05-07T12:00:00.000Z",
      "scopes": [
        "string"
      ],
      "token": "string",
      "user_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date | Token creation timestamp |
| `expires_in` | number | Seconds until expiration |
| `id` | number | Token ID |
| `last_used_at` | date | Last used timestamp |
| `name` | string | Token name |
| `revoked_at` | date | Token revocation timestamp |
| `scopes` | array<string> | Scopes granted to the token |
| `token` | string | Masked token value returned by Pachca |
| `user_id` | number | Pachca user ID associated with the token |

## Native endpoint

Through the native Pachca API, this operation is `GET /oauth/token/info` (base URL `https://api.pachca.com/api/shared/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-token-info.md) for the provider-specific parameters and requirements.

