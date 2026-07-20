# Digital Samba: Get default room settings

Retrieves default room settings from Digital Samba.

```
GET https://connect.mindcloud.co/v1/universal/digitalSamba/latest/actions/get-default-room-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Digital Samba `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/digitalSamba/latest/actions/get-default-room-settings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/digitalSamba/latest/actions/get-default-room-settings?${params}`, {
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
      "audioOnJoinEnabled": true,
      "backgroundColor": "string",
      "chatEnabled": true,
      "domain": "string",
      "fullScreenEnabled": true,
      "id": "string",
      "isLocked": true,
      "language": "string",
      "languageSelectionEnabled": true,
      "minimizeOwnTileEnabled": true,
      "ownerId": "string",
      "paletteMode": "string",
      "participantsListEnabled": true,
      "pinEnabled": true,
      "primaryColor": "string",
      "privateChatEnabled": true,
      "privateGroupChatEnabled": true,
      "privateGroupChatName": "Ava Chen",
      "screenshareEnabled": true,
      "toolbarColor": "string",
      "toolbarEnabled": true,
      "toolbarPosition": "string",
      "topbarEnabled": true,
      "videoOnJoinEnabled": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `audioOnJoinEnabled` | boolean |  |
| `backgroundColor` | string |  |
| `chatEnabled` | boolean |  |
| `domain` | string |  |
| `fullScreenEnabled` | boolean |  |
| `id` | string |  |
| `isLocked` | boolean |  |
| `language` | string |  |
| `languageSelectionEnabled` | boolean |  |
| `minimizeOwnTileEnabled` | boolean |  |
| `ownerId` | string |  |
| `paletteMode` | string |  |
| `participantsListEnabled` | boolean |  |
| `pinEnabled` | boolean |  |
| `primaryColor` | string |  |
| `privateChatEnabled` | boolean |  |
| `privateGroupChatEnabled` | boolean |  |
| `privateGroupChatName` | string |  |
| `screenshareEnabled` | boolean |  |
| `toolbarColor` | string |  |
| `toolbarEnabled` | boolean |  |
| `toolbarPosition` | string |  |
| `topbarEnabled` | boolean |  |
| `videoOnJoinEnabled` | boolean |  |

## Native endpoint

Through the native Digital Samba API, this operation is `GET /` (base URL `https://api.digitalsamba.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-default-room-settings.md) for the provider-specific parameters and requirements.

