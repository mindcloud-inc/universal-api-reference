# Discord: Remove Guild Member

Removes a member from a Discord guild.

```
DELETE https://connect.mindcloud.co/v1/universal/discord/latest/actions/remove-guild-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Discord `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/discord/latest/actions/remove-guild-member?connectionId=$CONNECTION_ID&guildId=string&userId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "guildId": "string",
  "userId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/discord/latest/actions/remove-guild-member?${params}`, {
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
| `userId` | string | yes | ID of the user/member to remove. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | string | Empty response body on success. |

## Native endpoint

Through the native Discord API, this operation is `DELETE /guilds/:guildId/members/:userId` (base URL `https://discord.com/api/v10`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-guild-member.md) for the provider-specific parameters and requirements.

