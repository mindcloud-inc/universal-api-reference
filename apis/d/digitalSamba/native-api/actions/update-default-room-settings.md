# Update default room settings with Digital Samba

Updates default room settings in Digital Samba.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/`
- **Base URL:** `https://api.digitalsamba.com/api/v1`
- **Official documentation:** [Update default room settings](https://developer.digitalsamba.com/rest-api/#default-room-settings-PATCHapi-v1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | no | JSON request body documented for this endpoint. |
| `domain` | body | `string` | no | Must contain only letters, numbers, dashes and underscores. Must not be one of docs, api, dev-api, staging-api, you, or dashboard Must be at least 3 characters. Must not be greater than 32 characters. |
| `virtual_backgrounds_enabled` | body | `string` | no | When enabled, participants on desktop devices will be able to appear on virtual backgrounds. |
| `default_role` | body | `string` | no | Select a role to be assigned to participants who join with no token (shared link to public room) or with a token without a role. Role ID or name. |
| `roles[]` | body | `array<string>` | no | Select a subset of roles for this room. The order in which they’re added will be the order in which they appear in the Participants panel. Must be an array of role IDs or names. Send multiple values as a array. |
| `is_locked` | body | `boolean` | no | Locked rooms require acceptance to join. Single-role rooms cannot be locked on join. |
| `session_length` | body | `number` | no | Value in minutes after which sessions should automatically end. Must be at least 1. Must not be greater than 1440. Empty value means Unlimited. |
| `topbar_enabled` | body | `boolean` | no | Set rooms with or without a top bar. |
| `pip_enabled` | body | `boolean` | no | When enabled, participants will be able to extract the video and audio tiles into a new window, so they can read or watch another application while they still monitor and look at the conference. Picture-in-picture is available only under Chrome desktop browser and not yet available in an embedded (iframe) scenario. |
| `auto_pip_enabled` | body | `boolean` | no | When enabled, Picture-in-Picture opens automatically when participants switch away from the main tab or app, keeping the video visible in a separate window while they work in another application. |
| `toolbar_enabled` | body | `boolean` | no | Set rooms with or without a toolbar. |
| `toolbar_position` | body | `string` | no | Choose your desired position for the toolbar or desktop devices. Must be one of left, right or bottom. |
| `toolbar_color` | body | `string` | no | Select a background colour for the toolbar in rooms. Must be color hex code. |
| `primary_color` | body | `string` | no | Select a colour for buttons and other interactive elements in rooms. Must be color hex code. |
| `background_color` | body | `string` | no | Select a colour for the background in rooms. Must be color hex code. |
| `palette_mode` | body | `string` | no | Palette mode (Appearance) will control the background colour of panels, modals and join screen. Must be one of light or dark. |
| `language` | body | `string` | no | Select a default language for the room’s UI. Must be one of ar-SA, ca-ES, en, es-ES, de-DE, it-IT, nb-NO, nl-NL, pt-PT, ro-RO, zh-CN or zh-TW. |
| `languages[]` | body | `array<string>` | no | Select a subset of languages for participants to be able to choose from. Must be an array of language codes. Send multiple values as a array. |
| `language_selection_enabled` | body | `boolean` | no | Allow each user to control application UI language on their side. |
| `room_reactions_enabled` | body | `boolean` | no | When enabled, all participants can use emoji reactions in this room. |
| `chat_reactions_enabled` | body | `boolean` | no | When enabled, participants can react to chat messages with emojis in this room. |
| `chat_reactions_extended_enabled` | body | `boolean` | no | When enabled, participants can react to chat messages using an expanded set of emojis in rooms. |
| `audio_on_join_enabled` | body | `boolean` | no | When disabled, users will join the session with muted microphones. |
| `video_on_join_enabled` | body | `boolean` | no | When disabled, users will join the session with turned-off cameras. |
| `hd_video_on_join_enabled` | body | `boolean` | no | Participants will stream in better quality. This setting requires more uplink bandwidth on the participants' side. |
| `hd_video_quality` | body | `string` | no | HD video quality. Must be one of 720_1.5, 720_2.5, 1080_2.5 or 1080_5.5. |
| `audio_quality` | body | `string` | no | Audio quality. Must be one of 32, 64, 128 or 256. |
| `audio_autogain_enabled` | body | `boolean` | no | Enable audio autogain. |
| `audio_noise_suppression_enabled` | body | `boolean` | no | When enabled, background noise will be reduced, resulting in clearer audio during the session. |
| `audio_echo_cancellation_enabled` | body | `boolean` | no | When enabled, echo and feedback will be eliminated, enhancing the clarity of communication during the session. |
| `mute_sound_enabled` | body | `boolean` | no | When enabled, participants will be able to mute locally the room sound. |
| `participants_list_enabled` | body | `boolean` | no | When enabled, your participants will have access to the Participants panel. |
| `pin_enabled` | body | `boolean` | no | When enabled, participants will have the option to select a participant to enlarge and continuously watch. |
| `full_screen_enabled` | body | `boolean` | no | Allow your participants to expand any participant tile to full screen. Will not work in Auto mode. |
| `minimize_own_tile_enabled` | body | `boolean` | no | Allow your participants to minimise and maximise their own tile when in tiled mode. |
| `minimize_own_tile_on_join_enabled` | body | `boolean` | no | When enabled, participants will join rooms with their own tile minimised. |
| `end_session_enabled` | body | `boolean` | no | When enabled, the "End session" button will be available in the toolbar. |
| `leave_session_enabled` | body | `boolean` | no | When enabled, the "Leave session" button will be available in the toolbar. |
| `rejoin_session_enabled` | body | `boolean` | no | When enabled, a "Rejoin" link will be shown after a user leaves a session. Otherwise only the 'You have left the session' text will be shown. |
| `connection_message_enabled` | body | `boolean` | no | When enabled, the "Connection message" status notification will be displayed in the session if a weak connection occurs. |
| `chat_enabled` | body | `boolean` | no | Allow participants to post and read in the public chat. |
| `private_chat_enabled` | body | `boolean` | no | Enable posting and reading in one-to-one chats with specific participants. |
| `private_group_chat_enabled` | body | `boolean` | no | Enable posting and reading in private group chats. |
| `private_group_chat_name` | body | `string` | no | Customise your private group chat with a name of your choice to be displayed. Must be at least 3 characters. |
| `private_group_chat_roles[]` | body | `array<string>` | yes | Must be an array of role IDs or names. Send multiple values as a array. |
| `chat_persistence_enabled` | body | `boolean` | no | When enabled, public chat messages from previous sessions in rooms are retained and reloaded when rooms are reopened. |
| `e2ee_enabled` | body | `boolean` | no | Secure usernames, chat messages, and video / audio streams, including shared screens with encryption keys that only participants in the room have access to. |
| `e2ee_badge_enabled` | body | `boolean` | no | Display an end-to-end encryption status badge in the meeting interface. When disabled, encryption status remains available in Settings. |
| `layout_mode_switch_enabled` | body | `boolean` | no | When disabled, participants will not see the layout mode switcher. |
| `simple_notifications_enabled` | body | `boolean` | no | Send participants non-disruptive notifications to inform them when others join and leave the session. |
| `join_screen_enabled` | body | `boolean` | no | When enabled, users will have the chance to test their speakers, camera and microphone ahead of joining. |
| `screenshare_enabled` | body | `boolean` | no | Allow your participants to share their screen. Mobile users will not be able to share their screen. |
| `recordings_enabled` | body | `boolean` | no | Allow participants to record sessions. |
| `recording_autostart_enabled` | body | `boolean` | no | When enabled, recording will automatically start when the first participant joins. |
| `recording_bookmarks_enabled` | body | `boolean` | no | When When enabled, bookmarks can be added during active recordings to highlight important moments. |
| `recording_breakout_autostart_enabled` | body | `boolean` | no | When enabled, automatically start recording breakout rooms when the first user joins. |
| `logo_enabled` | body | `boolean` | no | When enabled, the logo will be shown in rooms. |
| `custom_logo` | body | `string` | no | You may add a custom logo to be displayed in rooms and its recordings. Image URL or base64 encoded file source. |
| `application_logo` | body | `string` | no | You may add an application logo to be displayed in rooms join page. Image URL or base64 encoded file source. |
| `favicon` | body | `string` | no | You may add custom favicon to be displayed in rooms. Image URL or base64 encoded file source. |
| `recording_logo_enabled` | body | `boolean` | no | When enabled, the logo will be shown in recordings. |
