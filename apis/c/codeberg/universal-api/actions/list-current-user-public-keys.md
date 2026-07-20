# Codeberg: List Current User Public Keys



```
GET https://connect.mindcloud.co/v1/universal/codeberg/latest/actions/list-current-user-public-keys
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Codeberg `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/codeberg/latest/actions/list-current-user-public-keys?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/codeberg/latest/actions/list-current-user-public-keys?${params}`, {
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
      "fingerprint": "string",
      "id": 1,
      "key": "string",
      "key_type": "string",
      "read_only": true,
      "title": "string",
      "url": "https://example.com",
      "user": {
        "login": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date |  |
| `fingerprint` | string |  |
| `id` | number |  |
| `key` | string |  |
| `key_type` | string |  |
| `read_only` | boolean |  |
| `title` | string |  |
| `url` | string |  |
| `user.login` | string |  |

## Native endpoint

Through the native Codeberg API, this operation is `GET /user/keys` (base URL `https://codeberg.org/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-current-user-public-keys.md) for the provider-specific parameters and requirements.

