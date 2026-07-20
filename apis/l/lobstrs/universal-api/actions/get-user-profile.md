# lobst.rs: Get User Profile

Retrieves a user profile from lobst.rs.

```
GET https://connect.mindcloud.co/v1/universal/lobstrs/latest/actions/get-user-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a lobst.rs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lobstrs/latest/actions/get-user-profile?connectionId=$CONNECTION_ID&username=jcs" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "username": "jcs"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lobstrs/latest/actions/get-user-profile?${params}`, {
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
| `username` | string | yes | Lobsters username, such as jcs. Example: `jcs`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "about": "string",
      "avatar_url": "https://example.com",
      "created_at": "2026-05-07T12:00:00.000Z",
      "github_username": "Ava Chen",
      "invited_by_user": "string",
      "is_admin": true,
      "is_moderator": true,
      "karma": 1,
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `about` | string |  |
| `avatar_url` | string |  |
| `created_at` | date |  |
| `github_username` | string |  |
| `invited_by_user` | string |  |
| `is_admin` | boolean |  |
| `is_moderator` | boolean |  |
| `karma` | number |  |
| `username` | string |  |

## Native endpoint

Through the native lobst.rs API, this operation is `GET /~:username.json` (base URL `https://lobste.rs`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-profile.md) for the provider-specific parameters and requirements.

