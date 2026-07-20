# Discord-Bot: List Guild Members

Retrieves members from a Discord guild.

```
GET https://connect.mindcloud.co/v1/universal/discordBot/latest/actions/list-guild-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Discord-Bot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/discordBot/latest/actions/list-guild-members?connectionId=$CONNECTION_ID&guildId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "guildId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/discordBot/latest/actions/list-guild-members?${params}`, {
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
| `after` | string | no | Return members after this user ID. Discord defaults to 0 when omitted. |
| `guildId` | string | yes | Discord guild (server) ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deaf": true,
      "joined_at": "2026-05-07T12:00:00.000Z",
      "mute": true,
      "nick": "string",
      "pending": true,
      "roles": [
        "string"
      ],
      "user": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deaf` | boolean |  |
| `joined_at` | date |  |
| `mute` | boolean |  |
| `nick` | string |  |
| `pending` | boolean |  |
| `roles` | array<string> |  |
| `user` | object |  |

## Native endpoint

Through the native Discord-Bot API, this operation is `GET /guilds/:guildId/members` (base URL `https://discord.com/api/v10`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-guild-members.md) for the provider-specific parameters and requirements.

