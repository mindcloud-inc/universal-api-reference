# Codeberg: List Current User GPG Keys



```
GET https://connect.mindcloud.co/v1/universal/codeberg/latest/actions/list-current-user-gpg-keys
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Codeberg `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/codeberg/latest/actions/list-current-user-gpg-keys?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/codeberg/latest/actions/list-current-user-gpg-keys?${params}`, {
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
      "can_certify": true,
      "can_encrypt_comms": true,
      "can_encrypt_storage": true,
      "can_sign": true,
      "created_at": "2026-05-07T12:00:00.000Z",
      "emails": [
        {
          "email": "ava@example.com",
          "verified": true
        }
      ],
      "expires_at": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "key_id": "string",
      "primary_key_id": "string",
      "public_key": "string",
      "verified": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `can_certify` | boolean |  |
| `can_encrypt_comms` | boolean |  |
| `can_encrypt_storage` | boolean |  |
| `can_sign` | boolean |  |
| `created_at` | date |  |
| `emails[].email` | string |  |
| `emails[].verified` | boolean |  |
| `expires_at` | date |  |
| `id` | number |  |
| `key_id` | string |  |
| `primary_key_id` | string |  |
| `public_key` | string |  |
| `verified` | boolean |  |

## Native endpoint

Through the native Codeberg API, this operation is `GET /user/gpg_keys` (base URL `https://codeberg.org/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-current-user-gpg-keys.md) for the provider-specific parameters and requirements.

