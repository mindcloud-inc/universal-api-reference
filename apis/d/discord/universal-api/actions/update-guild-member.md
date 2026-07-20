# Discord: Update Guild Member

Updates a member in a Discord guild.

```
PUT https://connect.mindcloud.co/v1/universal/discord/latest/actions/update-guild-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Discord `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/discord/latest/actions/update-guild-member" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "guildId": "string",
  "userId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/discord/latest/actions/update-guild-member', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "guildId": "string",
    "userId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `guildId` | string | yes | ID of the guild. |
| `userId` | string | yes | ID of the user/member to modify. |
| `nick` | string | no | Value to set users nickname to. |
| `roles[]` | array<string> | no | Array of role IDs assigned to the member. |
| `mute` | boolean | no | Whether the user is muted in voice channels. |
| `deaf` | boolean | no | Whether the user is deafened in voice channels. |
| `channelId` | string | no | ID of voice channel to move user to (or null). |
| `communicationDisabledUntil` | date | no | ISO8601 timestamp for timeout expiration (or null). |

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

Through the native Discord API, this operation is `PATCH /guilds/:guildId/members/:userId` (base URL `https://discord.com/api/v10`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-guild-member.md) for the provider-specific parameters and requirements.

