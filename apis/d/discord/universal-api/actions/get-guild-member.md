# Discord: Get Guild Member

Retrieves a Discord guild member by user ID.

```
GET https://connect.mindcloud.co/v1/universal/discord/latest/actions/get-guild-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Discord `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/discord/latest/actions/get-guild-member?connectionId=$CONNECTION_ID&guildId=string&userId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "guildId": "string",
  "userId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/discord/latest/actions/get-guild-member?${params}`, {
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
| `userId` | string | yes | ID of the user/member. |

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
| `user.id` | string |  |
| `user.publicFlags` | number |  |
| `user.username` | string |  |

## Native endpoint

Through the native Discord API, this operation is `GET /guilds/:guildId/members/:userId` (base URL `https://discord.com/api/v10`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-guild-member.md) for the provider-specific parameters and requirements.

