# Digital Samba: Update default room settings

Updates default room settings in Digital Samba.

```
PUT https://connect.mindcloud.co/v1/universal/digitalSamba/latest/actions/update-default-room-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Digital Samba `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/digitalSamba/latest/actions/update-default-room-settings" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "privateGroupChatRoles[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/digitalSamba/latest/actions/update-default-room-settings', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "privateGroupChatRoles[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `virtualBackgroundsEnabled` | string | no | When enabled, participants on desktop devices will be able to appear on virtual backgrounds. |
| `privateGroupChatRoles[]` | array<string> | yes | Must be an array of role IDs or names. Accepts multiple values as an array. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `body` | object | no | JSON request body documented for this endpoint. |
| `domain` | string | no | Must contain only letters, numbers, dashes and underscores. Must not be one of docs, api, dev-api, staging-api, you, or dashboard Must be at least 3 characters. Must not be greater than 32 characters. |
| `defaultRole` | string | no | Select a role to be assigned to participants who join with no token (shared link to public room) or with a token without a role. Role ID or name. |
| `roles[]` | array<string> | no | Select a subset of roles for this room. The order in which they’re added will be the order in which they appear in the Participants panel. Must be an array of role IDs or names. Accepts multiple values as an array. |
| `isLocked` | boolean | no | Locked rooms require acceptance to join. Single-role rooms cannot be locked on join. |
| `sessionLength` | number | no | Value in minutes after which sessions should automatically end. Must be at least 1. Must not be greater than 1440. Empty value means Unlimited. |
| `topbarEnabled` | boolean | no | Set rooms with or without a top bar. |
| `pipEnabled` | boolean | no | When enabled, participants will be able to extract the video and audio tiles into a new window, so they can read or watch another application while they still monitor and look at the conference. Picture-in-picture is available only under Chrome desktop browser and not yet available in an embedded (iframe) scenario. |
| `autoPipEnabled` | boolean | no | When enabled, Picture-in-Picture opens automatically when participants switch away from the main tab or app, keeping the video visible in a separate window while they work in another application. |
| `toolbarEnabled` | boolean | no | Set rooms with or without a toolbar. |
| `toolbarPosition` | string | no | Choose your desired position for the toolbar or desktop devices. Must be one of left, right or bottom. |
| `toolbarColor` | string | no | Select a background colour for the toolbar in rooms. Must be color hex code. |
| `primaryColor` | string | no | Select a colour for buttons and other interactive elements in rooms. Must be color hex code. |
| `backgroundColor` | string | no | Select a colour for the background in rooms. Must be color hex code. |
| `paletteMode` | string | no | Palette mode (Appearance) will control the background colour of panels, modals and join screen. Must be one of light or dark. |
| `language` | string | no | Select a default language for the room’s UI. Must be one of ar-SA, ca-ES, en, es-ES, de-DE, it-IT, nb-NO, nl-NL, pt-PT, ro-RO, zh-CN or zh-TW. |
| `languages[]` | array<string> | no | Select a subset of languages for participants to be able to choose from. Must be an array of language codes. Accepts multiple values as an array. |
| `languageSelectionEnabled` | boolean | no | Allow each user to control application UI language on their side. |
| `roomReactionsEnabled` | boolean | no | When enabled, all participants can use emoji reactions in this room. |
| `chatReactionsEnabled` | boolean | no | When enabled, participants can react to chat messages with emojis in this room. |
| `chatReactionsExtendedEnabled` | boolean | no | When enabled, participants can react to chat messages using an expanded set of emojis in rooms. |
| `audioOnJoinEnabled` | boolean | no | When disabled, users will join the session with muted microphones. |
| `videoOnJoinEnabled` | boolean | no | When disabled, users will join the session with turned-off cameras. |
| `hdVideoOnJoinEnabled` | boolean | no | Participants will stream in better quality. This setting requires more uplink bandwidth on the participants' side. |
| `hdVideoQuality` | string | no | HD video quality. Must be one of 720_1.5, 720_2.5, 1080_2.5 or 1080_5.5. |
| `audioQuality` | string | no | Audio quality. Must be one of 32, 64, 128 or 256. |
| `audioAutogainEnabled` | boolean | no | Enable audio autogain. |
| `audioNoiseSuppressionEnabled` | boolean | no | When enabled, background noise will be reduced, resulting in clearer audio during the session. |
| `audioEchoCancellationEnabled` | boolean | no | When enabled, echo and feedback will be eliminated, enhancing the clarity of communication during the session. |
| `muteSoundEnabled` | boolean | no | When enabled, participants will be able to mute locally the room sound. |
| `participantsListEnabled` | boolean | no | When enabled, your participants will have access to the Participants panel. |
| `pinEnabled` | boolean | no | When enabled, participants will have the option to select a participant to enlarge and continuously watch. |
| `fullScreenEnabled` | boolean | no | Allow your participants to expand any participant tile to full screen. Will not work in Auto mode. |
| `minimizeOwnTileEnabled` | boolean | no | Allow your participants to minimise and maximise their own tile when in tiled mode. |
| `minimizeOwnTileOnJoinEnabled` | boolean | no | When enabled, participants will join rooms with their own tile minimised. |
| `endSessionEnabled` | boolean | no | When enabled, the "End session" button will be available in the toolbar. |
| `leaveSessionEnabled` | boolean | no | When enabled, the "Leave session" button will be available in the toolbar. |
| `rejoinSessionEnabled` | boolean | no | When enabled, a "Rejoin" link will be shown after a user leaves a session. Otherwise only the 'You have left the session' text will be shown. |
| `connectionMessageEnabled` | boolean | no | When enabled, the "Connection message" status notification will be displayed in the session if a weak connection occurs. |
| `chatEnabled` | boolean | no | Allow participants to post and read in the public chat. |
| `privateChatEnabled` | boolean | no | Enable posting and reading in one-to-one chats with specific participants. |
| `privateGroupChatEnabled` | boolean | no | Enable posting and reading in private group chats. |
| `privateGroupChatName` | string | no | Customise your private group chat with a name of your choice to be displayed. Must be at least 3 characters. |
| `chatPersistenceEnabled` | boolean | no | When enabled, public chat messages from previous sessions in rooms are retained and reloaded when rooms are reopened. |
| `e2eeEnabled` | boolean | no | Secure usernames, chat messages, and video / audio streams, including shared screens with encryption keys that only participants in the room have access to. |
| `e2eeBadgeEnabled` | boolean | no | Display an end-to-end encryption status badge in the meeting interface. When disabled, encryption status remains available in Settings. |
| `layoutModeSwitchEnabled` | boolean | no | When disabled, participants will not see the layout mode switcher. |
| `simpleNotificationsEnabled` | boolean | no | Send participants non-disruptive notifications to inform them when others join and leave the session. |
| `joinScreenEnabled` | boolean | no | When enabled, users will have the chance to test their speakers, camera and microphone ahead of joining. |
| `screenshareEnabled` | boolean | no | Allow your participants to share their screen. Mobile users will not be able to share their screen. |
| `recordingsEnabled` | boolean | no | Allow participants to record sessions. |
| `recordingAutostartEnabled` | boolean | no | When enabled, recording will automatically start when the first participant joins. |
| `recordingBookmarksEnabled` | boolean | no | When When enabled, bookmarks can be added during active recordings to highlight important moments. |
| `recordingBreakoutAutostartEnabled` | boolean | no | When enabled, automatically start recording breakout rooms when the first user joins. |
| `logoEnabled` | boolean | no | When enabled, the logo will be shown in rooms. |
| `customLogo` | string | no | You may add a custom logo to be displayed in rooms and its recordings. Image URL or base64 encoded file source. |
| `applicationLogo` | string | no | You may add an application logo to be displayed in rooms join page. Image URL or base64 encoded file source. |
| `favicon` | string | no | You may add custom favicon to be displayed in rooms. Image URL or base64 encoded file source. |
| `recordingLogoEnabled` | boolean | no | When enabled, the logo will be shown in recordings. |

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

Through the native Digital Samba API, this operation is `PATCH /` (base URL `https://api.digitalsamba.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-default-room-settings.md) for the provider-specific parameters and requirements.

