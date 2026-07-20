# Discord-Bot: Get Current Bot User

Retrieves the current bot user from Discord.

```
GET https://connect.mindcloud.co/v1/universal/discordBot/latest/actions/get-current-bot-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Discord-Bot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/discordBot/latest/actions/get-current-bot-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/discordBot/latest/actions/get-current-bot-user?${params}`, {
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
      "bot": true,
      "global_name": "Ava Chen",
      "id": "string",
      "locale": "string",
      "username": "Ava Chen",
      "verified": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bot` | boolean |  |
| `global_name` | string |  |
| `id` | string |  |
| `locale` | string |  |
| `username` | string |  |
| `verified` | boolean |  |

## Native endpoint

Through the native Discord-Bot API, this operation is `GET /users/@me` (base URL `https://discord.com/api/v10`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-bot-user.md) for the provider-specific parameters and requirements.

