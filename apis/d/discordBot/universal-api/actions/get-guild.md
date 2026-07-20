# Discord-Bot: Get Guild

Retrieves a Discord guild by ID.

```
GET https://connect.mindcloud.co/v1/universal/discordBot/latest/actions/get-guild
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Discord-Bot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/discordBot/latest/actions/get-guild?connectionId=$CONNECTION_ID&guildId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "guildId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/discordBot/latest/actions/get-guild?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "features": [
        "string"
      ],
      "id": "string",
      "name": "Ava Chen",
      "owner_id": "string",
      "preferred_locale": "string",
      "roles": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `features` | array<string> |  |
| `id` | string |  |
| `name` | string |  |
| `owner_id` | string |  |
| `preferred_locale` | string |  |
| `roles` | array<object> |  |

## Native endpoint

Through the native Discord-Bot API, this operation is `GET /guilds/:guildId` (base URL `https://discord.com/api/v10`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-guild.md) for the provider-specific parameters and requirements.

