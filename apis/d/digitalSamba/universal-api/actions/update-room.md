# Digital Samba: Update room

Updates an existing room in Digital Samba.

```
PUT https://connect.mindcloud.co/v1/universal/digitalSamba/latest/actions/update-room
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Digital Samba `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/digitalSamba/latest/actions/update-room" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "room": "string",
  "privacy": "string",
  "privateGroupChatRoles[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/digitalSamba/latest/actions/update-room', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "room": "string",
    "privacy": "string",
    "privateGroupChatRoles[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `room` | string | yes | Room path parameter. |
| `privacy` | string | yes | Public rooms can be joined using a room link. Private rooms require the room link to include a valid token. Must be in ['public', 'private']. |
| `privateGroupChatRoles[]` | array<string> | yes | Must be an array of role IDs or names. Accepts multiple values as an array. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `body` | object | no | JSON request body documented for this endpoint. |
| `description` | string | no | Must be at least 3 characters. Must not be greater than 500 characters. |
| `friendlyUrl` | string | no | Must be unique. Must be at least 3 characters. Must not be greater than 32 characters. |
| `externalId` | string | no | Assign the room with an ID for integration on your side. |
| `defaultRole` | string | no | Select a role to be assigned to participants who join with no token (shared link to public room) or with a token without a role. Role ID or name. |
| `roles[]` | array<string> | no | Select a subset of roles for this room. The order in which they’re added will be the order in which they appear in the Participants panel. Must be an array of role IDs or names. Accepts multiple values as an array. |
| `isLocked` | boolean | no | Locked rooms require acceptance to join. Single-role rooms cannot be locked on join. |
| `topbarEnabled` | boolean | no | Set the room with or without a top bar. |
| `toolbarEnabled` | boolean | no | Set the room with or without a toolbar. |
| `toolbarPosition` | string | no | Choose your desired position for the toolbar for desktop devices. Must be one of left, right or bottom. |
| `toolbarColor` | string | no | Select a background colour for the toolbar in this room. Must be color hex code. |
| `primaryColor` | string | no | Select a colour for buttons and other interactive elements in this room. Must be color hex code. |
| `backgroundColor` | string | no | Select a colour for the background in this room. Must be color hex code. |
| `paletteMode` | string | no | Palette mode (Appearance) will control the background colour of panels, modals and join screen. Must be one of light or dark. |
| `language` | string | no | Select a default language for the room’s UI. Must be one of ar-SA, en, es-ES, de-DE, it-IT, nl-NL, pt-PT, ro-RO, zh-CN or zh-TW. |
| `audioOnJoinEnabled` | boolean | no | When disabled, users will join the session with muted microphones. |
| `videoOnJoinEnabled` | boolean | no | When disabled, users will join the session with turned-off cameras. |
| `screenshareEnabled` | boolean | no | Allow your participants to share their screen. Mobile users will not be able to share their screen. |
| `participantsListEnabled` | boolean | no | When enabled, your participants will have access to the Participants panel. |
| `recordingsEnabled` | boolean | no | Allow participants to record sessions. |
| `logoEnabled` | boolean | no | When enabled, the logo will be shown in this room. |
| `virtualBackgroundsEnabled` | boolean | no | When enabled, participants on desktop devices will be able to appear on virtual backgrounds. |
| `raiseHandEnabled` | boolean | no | Allow participants to raise hand to take turns to speak without disrupting this session. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "audioOnJoinEnabled": true,
      "backgroundColor": "string",
      "customLogo": "string",
      "description": "string",
      "friendlyUrl": "https://example.com",
      "id": "string",
      "isLocked": true,
      "language": "string",
      "languageSelectionEnabled": true,
      "logoEnabled": true,
      "maxBroadcasters": 1,
      "maxParticipants": 1,
      "paletteMode": "string",
      "participantsListEnabled": true,
      "primaryColor": "string",
      "privacy": "string",
      "recordingLogoEnabled": true,
      "recordingsEnabled": true,
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
| `customLogo` | string |  |
| `description` | string |  |
| `friendlyUrl` | string |  |
| `id` | string |  |
| `isLocked` | boolean |  |
| `language` | string |  |
| `languageSelectionEnabled` | boolean |  |
| `logoEnabled` | boolean |  |
| `maxBroadcasters` | number |  |
| `maxParticipants` | number |  |
| `paletteMode` | string |  |
| `participantsListEnabled` | boolean |  |
| `primaryColor` | string |  |
| `privacy` | string |  |
| `recordingLogoEnabled` | boolean |  |
| `recordingsEnabled` | boolean |  |
| `screenshareEnabled` | boolean |  |
| `toolbarColor` | string |  |
| `toolbarEnabled` | boolean |  |
| `toolbarPosition` | string |  |
| `topbarEnabled` | boolean |  |
| `videoOnJoinEnabled` | boolean |  |

## Native endpoint

Through the native Digital Samba API, this operation is `PATCH /rooms/:room` (base URL `https://api.digitalsamba.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-room.md) for the provider-specific parameters and requirements.

