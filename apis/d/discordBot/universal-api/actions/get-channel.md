# Discord-Bot: Get Channel

Retrieves a Discord channel by ID.

```
GET https://connect.mindcloud.co/v1/universal/discordBot/latest/actions/get-channel
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Discord-Bot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/discordBot/latest/actions/get-channel?connectionId=$CONNECTION_ID&channelId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "channelId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/discordBot/latest/actions/get-channel?${params}`, {
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
| `channelId` | string | yes | Discord channel ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "guild_id": "string",
      "id": "string",
      "name": "Ava Chen",
      "nsfw": true,
      "parent_id": "string",
      "position": 1,
      "topic": "string",
      "type": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `guild_id` | string |  |
| `id` | string |  |
| `name` | string |  |
| `nsfw` | boolean |  |
| `parent_id` | string |  |
| `position` | number |  |
| `topic` | string |  |
| `type` | number |  |

## Native endpoint

Through the native Discord-Bot API, this operation is `GET /channels/:channelId` (base URL `https://discord.com/api/v10`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-channel.md) for the provider-specific parameters and requirements.

