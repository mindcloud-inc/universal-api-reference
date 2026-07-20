# Discord: Get Current User

Retrieves the current authenticated Discord user.

```
GET https://connect.mindcloud.co/v1/universal/discord/latest/actions/get-current-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Discord `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/discord/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/discord/latest/actions/get-current-user?${params}`, {
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
      "accentColor": 1,
      "avatar": "string",
      "avatarDecorationData": {},
      "banner": "string",
      "bannerColor": "string",
      "clan": {},
      "collectibles": {},
      "discriminator": "string",
      "displayNameStyles": {},
      "flags": 1,
      "globalName": "Ava Chen",
      "id": "string",
      "locale": "string",
      "mfaEnabled": true,
      "premiumType": 1,
      "primaryGuild": {},
      "publicFlags": 1,
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accentColor` | number |  |
| `avatar` | string |  |
| `avatarDecorationData` | object |  |
| `banner` | string |  |
| `bannerColor` | string |  |
| `clan` | object |  |
| `collectibles` | object |  |
| `discriminator` | string |  |
| `displayNameStyles` | object |  |
| `flags` | number |  |
| `globalName` | string |  |
| `id` | string |  |
| `locale` | string |  |
| `mfaEnabled` | boolean |  |
| `premiumType` | number |  |
| `primaryGuild` | object |  |
| `publicFlags` | number |  |
| `username` | string |  |

## Native endpoint

Through the native Discord API, this operation is `GET /users/@me` (base URL `https://discord.com/api/v10`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-user.md) for the provider-specific parameters and requirements.

