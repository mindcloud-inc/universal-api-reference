# Bonusly: Search Users

Finds users in Bonusly by search term.

```
GET https://connect.mindcloud.co/v1/universal/bonusly/latest/actions/search-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bonusly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bonusly/latest/actions/search-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bonusly/latest/actions/search-users?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `search` | string | no | Search text for user autocomplete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "canReceive": true,
      "displayName": "Ava Chen",
      "email": "ava@example.com",
      "fullPicUrl": "https://example.com",
      "id": "string",
      "profilePicUrl": "https://example.com",
      "userMode": "string",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `canReceive` | boolean |  |
| `displayName` | string |  |
| `email` | string |  |
| `fullPicUrl` | string |  |
| `id` | string |  |
| `profilePicUrl` | string |  |
| `userMode` | string |  |
| `username` | string |  |

## Native endpoint

Through the native Bonusly API, this operation is `GET /users/autocomplete` (base URL `https://bonus.ly/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-users.md) for the provider-specific parameters and requirements.

