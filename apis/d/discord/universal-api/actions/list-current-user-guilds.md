# Discord: List Current User Guilds

Lists the current user's guilds in Discord.

```
GET https://connect.mindcloud.co/v1/universal/discord/latest/actions/list-current-user-guilds
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Discord `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/discord/latest/actions/list-current-user-guilds?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/discord/latest/actions/list-current-user-guilds?${params}`, {
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
| `limit` | number | no | Maximum number of guilds to return (1-200). Example: `50`. |
| `withCounts` | boolean | no | Include approximate member and presence counts. Example: `false`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `before` | string | no | Get guilds before this guild ID. Example: `123456789012345678`. |
| `after` | string | no | Get guilds after this guild ID. Example: `123456789012345678`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "banner": "string",
      "features": [
        "string"
      ],
      "icon": "string",
      "id": "string",
      "name": "Ava Chen",
      "owner": true,
      "permissions": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `banner` | string |  |
| `features` | array<string> |  |
| `icon` | string |  |
| `id` | string |  |
| `name` | string |  |
| `owner` | boolean |  |
| `permissions` | string |  |

## Native endpoint

Through the native Discord API, this operation is `GET /users/@me/guilds` (base URL `https://discord.com/api/v10`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-current-user-guilds.md) for the provider-specific parameters and requirements.

