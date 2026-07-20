# Create a new room with Digital Samba

Creates a new room in Digital Samba.

## Endpoint

- **Method:** `POST`
- **Path:** `/rooms`
- **Base URL:** `https://api.digitalsamba.com/api/v1`
- **Official documentation:** [Create a new room](https://developer.digitalsamba.com/rest-api/#rooms-POSTapi-v1-rooms)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | no | JSON request body documented for this endpoint. |
| `privacy` | body | `string` | yes | Public rooms can be joined using a room link. Private rooms require the room link to include a valid token. Must be in ['public', 'private']. |
| `roles[]` | body | `array<string>` | yes | Select a subset of roles for this room. The order in which they’re added will be the order in which they appear in the Participants panel. Must be an array of role IDs or names. Send multiple values as a array. |
| `private_group_chat_roles[]` | body | `array<string>` | yes | Must be an array of role IDs or names. Send multiple values as a array. |
| `description` | body | `string` | no | Must be at least 3 characters. Must not be greater than 500 characters. |
| `friendly_url` | body | `string` | no | Must be unique. Must be at least 3 characters. Must not be greater than 32 characters. |
| `external_id` | body | `string` | no | Assign the room with an ID for integration on your side. |
| `default_role` | body | `string` | no | Select a role to be assigned to participants who join with no token (shared link to public room) or with a token without a role. Role ID or name. |
| `tags[]` | body | `array<string>` | no | Must be an array of room tags. Send multiple values as a array. |
| `is_locked` | body | `boolean` | no | Locked rooms require acceptance to join. Single-role rooms cannot be locked on join. |
| `topbar_enabled` | body | `boolean` | no | Set the room with or without a top bar. |
| `toolbar_enabled` | body | `boolean` | no | Set the room with or without a toolbar. |
| `toolbar_position` | body | `string` | no | Choose your desired position for the toolbar for desktop devices. Must be one of left, right or bottom. |
| `toolbar_color` | body | `string` | no | Select a background colour for the toolbar in this room. Must be color hex code. |
| `primary_color` | body | `string` | no | Select a colour for buttons and other interactive elements in this room. Must be color hex code. |
| `background_color` | body | `string` | no | Select a colour for the background in this room. Must be color hex code. |
| `palette_mode` | body | `string` | no | Palette mode (Appearance) will control the background colour of panels, modals and join screen. Must be one of light or dark. |
| `language` | body | `string` | no | Select a default language for the room’s UI. Must be one of ar-SA, en, es-ES, de-DE, it-IT, nl-NL, pt-PT, ro-RO, zh-CN or zh-TW. |
| `audio_on_join_enabled` | body | `boolean` | no | When disabled, users will join the session with muted microphones. |
| `video_on_join_enabled` | body | `boolean` | no | When disabled, users will join the session with turned-off cameras. |
| `screenshare_enabled` | body | `boolean` | no | Allow your participants to share their screen. Mobile users will not be able to share their screen. |
| `participants_list_enabled` | body | `boolean` | no | When enabled, your participants will have access to the Participants panel. |
| `recordings_enabled` | body | `boolean` | no | Allow participants to record sessions. |
| `logo_enabled` | body | `boolean` | no | When enabled, the logo will be shown in this room. |
| `virtual_backgrounds_enabled` | body | `boolean` | no | When enabled, participants on desktop devices will be able to appear on virtual backgrounds. |
