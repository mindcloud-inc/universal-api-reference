# Discord-Bot: Search Guild Members

Finds Discord guild members by username or nickname prefix.

```
GET https://connect.mindcloud.co/v1/universal/discordBot/latest/actions/search-guild-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Discord-Bot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/discordBot/latest/actions/search-guild-members?connectionId=$CONNECTION_ID&guildId=string&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "guildId": "string",
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/discordBot/latest/actions/search-guild-members?${params}`, {
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
| `guildId` | string | yes | Discord guild (server) ID. |
| `query` | string | yes | Username or nickname prefix to search for. |

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

Through the native Discord-Bot API, this operation is `GET /guilds/:guildId/members/search` (base URL `https://discord.com/api/v10`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-guild-members.md) for the provider-specific parameters and requirements.

