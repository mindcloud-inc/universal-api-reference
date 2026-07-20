# BugHerd: List Users

Retrieves users from BugHerd.

```
GET https://connect.mindcloud.co/v1/universal/bugHerd/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BugHerd `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bugHerd/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bugHerd/latest/actions/list-users?${params}`, {
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
      "avatarUrl": "https://example.com",
      "displayName": "Ava Chen",
      "email": "ava@example.com",
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avatarUrl` | string |  |
| `displayName` | string |  |
| `email` | string |  |
| `id` | number |  |

## Native endpoint

Through the native BugHerd API, this operation is `GET users.json` (base URL `https://www.bugherd.com/api_v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

