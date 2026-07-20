# Update Conference with ClickMeeting

Updates a conference in ClickMeeting by room ID.

## Endpoint

- **Method:** `PUT`
- **Path:** `conferences/{{room_id}}`
- **Base URL:** `https://api.clickmeeting.com/v1`
- **Official documentation:** [Update Conference](https://dev.clickmeeting.com/api-doc/#put_conferences_by_room_id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `room_id` | path | `number` | yes | Conference room identifier. |
| `name` | body | `string` | no | Updated room name. |
| `room_type` | body | `list` | no | Updated room type. Accepted values: `meeting`, `webinar`. |
| `permanent_room` | body | `boolean` | no | Required when changing starts_at or duration. |
| `access_type` | body | `list<number>` | no | Updated room access model. Accepted values: `1`, `2`, `3`. |
| `lobby_description` | body | `string` | no | Updated lobby message. |
| `lobby_enabled` | body | `boolean` | no | Turn the lobby on or off. |
| `starts_at` | body | `date` | no | Updated conference start timestamp. |
| `duration` | body | `string` | no | Updated duration, for example 1:20 or 0:20. |
| `timezone` | body | `string` | no | Updated conference time zone. |
| `skin_id` | body | `number` | no | Updated skin identifier. |
| `password` | body | `string` | no | Updated room password. |
| `status` | body | `list` | no | Activate or deactivate the conference. Accepted values: `active`, `inactive`. |
| `registration.enabled` | body | `boolean` | no | Enable or disable registration. |
| `registration.template` | body | `list<number>` | no | Updated registration template ID. Accepted values: `1`, `2`, `3`. |
| `settings.show_on_personal_page` | body | `boolean` | no | Display the conference on the personal page. |
| `settings.thank_you_emails_enabled` | body | `boolean` | no | Send thank-you emails after the conference. |
| `settings.connection_tester_enabled` | body | `boolean` | no | Enable the connection tester. |
| `settings.phonegateway_enabled` | body | `boolean` | no | Enable dial-in phone gateways. |
| `settings.recorder_autostart_enabled` | body | `boolean` | no | Auto-start the recorder. |
| `settings.room_invite_button_enabled` | body | `boolean` | no | Show the room invite button. |
| `settings.social_media_sharing_enabled` | body | `boolean` | no | Allow social sharing from the room. |
| `settings.connection_status_enabled` | body | `boolean` | no | Show attendee connection status. |
| `settings.thank_you_page_url` | body | `string` | no | Optional custom thank-you page URL. |
