# Discord-Bot: Delete Channel

Deletes or closes a Discord channel.

```
DELETE https://connect.mindcloud.co/v1/universal/discordBot/latest/actions/delete-channel
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Discord-Bot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/discordBot/latest/actions/delete-channel?connectionId=$CONNECTION_ID&channelId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "channelId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/discordBot/latest/actions/delete-channel?${params}`, {
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
| `position` | number |  |
| `topic` | string |  |
| `type` | number |  |

## Native endpoint

Through the native Discord-Bot API, this operation is `DELETE /channels/:channelId` (base URL `https://discord.com/api/v10`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-channel.md) for the provider-specific parameters and requirements.

