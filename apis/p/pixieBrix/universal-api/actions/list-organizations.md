# PixieBrix: List Organizations

Retrieves the current user's organizations from PixieBrix.

```
GET https://connect.mindcloud.co/v1/universal/pixieBrix/latest/actions/list-organizations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PixieBrix `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pixieBrix/latest/actions/list-organizations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pixieBrix/latest/actions/list-organizations?${params}`, {
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
      "ai_default_chat_copilot": true,
      "default_role": 1,
      "enable_invitations": true,
      "enforce_update_millis": 1,
      "id": "string",
      "members": [
        {}
      ],
      "name": "Ava Chen",
      "scope": "string",
      "session_idle_timeout_minutes": 1,
      "trial_end_timestamp": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ai_default_chat_copilot` | boolean |  |
| `default_role` | number |  |
| `enable_invitations` | boolean |  |
| `enforce_update_millis` | number |  |
| `id` | string |  |
| `members` | array<object> |  |
| `name` | string |  |
| `scope` | string |  |
| `session_idle_timeout_minutes` | number |  |
| `trial_end_timestamp` | date |  |

## Native endpoint

Through the native PixieBrix API, this operation is `GET /api/organizations/` (base URL `https://app.pixiebrix.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-organizations.md) for the provider-specific parameters and requirements.

