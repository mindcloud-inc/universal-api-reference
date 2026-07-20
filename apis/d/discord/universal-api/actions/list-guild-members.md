# Discord: List Guild Members

Lists members in a Discord guild.

```
GET https://connect.mindcloud.co/v1/universal/discord/latest/actions/list-guild-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Discord `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/discord/latest/actions/list-guild-members?connectionId=$CONNECTION_ID&guildId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "guildId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/discord/latest/actions/list-guild-members?${params}`, {
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
| `guildId` | string | yes | ID of the guild. |
| `limit` | number | no | Max members to return (1-1000). Default: `100`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `after` | string | no | Return members after this user ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deaf": true,
      "flags": 1,
      "joinedAt": "2026-05-07T12:00:00.000Z",
      "mute": true,
      "pending": true,
      "roles": [
        "string"
      ],
      "user": {
        "avatar": "string",
        "bot": true,
        "discriminator": "string",
        "flags": 1,
        "globalName": "Ava Chen",
        "id": "string",
        "publicFlags": 1,
        "username": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deaf` | boolean |  |
| `flags` | number |  |
| `joinedAt` | date |  |
| `mute` | boolean |  |
| `pending` | boolean |  |
| `roles` | array<string> |  |
| `user` | object |  |
| `user.avatar` | string |  |
| `user.bot` | boolean |  |
| `user.discriminator` | string |  |
| `user.flags` | number |  |
| `user.globalName` | string |  |
| `user.id` | string |  |
| `user.publicFlags` | number |  |
| `user.username` | string |  |

## Native endpoint

Through the native Discord API, this operation is `GET /guilds/:guildId/members` (base URL `https://discord.com/api/v10`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-guild-members.md) for the provider-specific parameters and requirements.

