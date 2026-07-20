# Dev.to: List Followers

Lists the followers of the authenticated Dev.to user.

```
GET https://connect.mindcloud.co/v1/universal/devto/latest/actions/list-followers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dev.to `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/devto/latest/actions/list-followers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/devto/latest/actions/list-followers?${params}`, {
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
      "id": 1,
      "name": "Ava Chen",
      "path": "https://example.com",
      "profile_image": "string",
      "type_of": "string",
      "user_id": 1,
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date | When the follow relationship was created. |
| `id` | number | Follow relationship ID. |
| `name` | string | The follower's display name. |
| `path` | string | Path to the follower's DEV profile. |
| `profile_image` | string | Profile image URL or path. |
| `type_of` | string | Follower record type. |
| `user_id` | number | The follower's user ID. |
| `username` | string | The follower's DEV username. |

## Native endpoint

Through the native Dev.to API, this operation is `GET /followers/users` (base URL `https://dev.to/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-followers.md) for the provider-specific parameters and requirements.

