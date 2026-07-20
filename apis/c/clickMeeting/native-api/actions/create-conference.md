# Create Conference with ClickMeeting

Creates a new conference in ClickMeeting.

## Endpoint

- **Method:** `POST`
- **Path:** `conferences`
- **Base URL:** `https://api.clickmeeting.com/v1`
- **Official documentation:** [Create Conference](https://dev.clickmeeting.com/api-doc/#post_conferences)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Room name shown to attendees. |
| `room_type` | body | `list` | yes | Choose whether to create a meeting or webinar room. Accepted values: `meeting`, `webinar`. |
| `permanent_room` | body | `boolean` | yes | Use true for a permanent room, false for a scheduled room. |
| `access_type` | body | `list<number>` | yes | Choose the room access model. Accepted values: `1`, `2`, `3`. |
| `custom_room_url_name` | body | `string` | no | Optional custom room URL suffix. |
| `lobby_description` | body | `string` | no | Optional lobby message shown before the room starts. |
| `lobby_enabled` | body | `boolean` | no | Turn the lobby on or off. |
| `starts_at` | body | `date` | no | Scheduled conference start timestamp. |
| `duration` | body | `string` | no | Conference duration, for example 1:20 or 0:20. |
| `timezone` | body | `string` | no | Conference time zone, for example America/New_York. |
| `skin_id` | body | `number` | no | Optional room skin identifier. |
| `password` | body | `string` | no | Required only for password-protected rooms. |
| `registration.enabled` | body | `boolean` | no | Enable or disable attendee registration. |
| `registration.template` | body | `list<number>` | no | Optional registration template ID. Accepted values: `1`, `2`, `3`. |
| `settings.show_on_personal_page` | body | `boolean` | no | Display the conference on the personal page. |
| `settings.thank_you_emails_enabled` | body | `boolean` | no | Send thank-you emails after the conference. |
| `settings.connection_tester_enabled` | body | `boolean` | no | Enable the connection tester. |
| `settings.phonegateway_enabled` | body | `boolean` | no | Enable dial-in phone gateways. |
| `settings.recorder_autostart_enabled` | body | `boolean` | no | Auto-start the recorder. |
| `settings.room_invite_button_enabled` | body | `boolean` | no | Show the room invite button. |
| `settings.social_media_sharing_enabled` | body | `boolean` | no | Allow social sharing from the room. |
| `settings.connection_status_enabled` | body | `boolean` | no | Show attendee connection status. |
| `settings.thank_you_page_url` | body | `string` | no | Optional custom thank-you page URL. |
| `settings.encryption_enabled` | body | `boolean` | no | Enable end-to-end encryption. |
