# Generate Conference Auto-Login URL with ClickMeeting

Creates an auto-login URL for a conference in ClickMeeting.

## Endpoint

- **Method:** `POST`
- **Path:** `conferences/{{room_id}}/room/autologin_hash`
- **Base URL:** `https://api.clickmeeting.com/v1`
- **Official documentation:** [Generate Conference Auto-Login URL](https://dev.clickmeeting.com/api-doc/#post_autologin_hash)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `room_id` | path | `number` | yes | Conference room identifier. |
| `email` | body | `string` | yes | Attendee email address. |
| `nickname` | body | `string` | yes | Attendee nickname. |
| `role` | body | `list` | yes | Conference role for the generated auto-login link. Accepted values: `guest_speaker`, `host`, `listener`, `moderator`, `presenter`. |
| `password` | body | `string` | no | Room password when access_type=2. |
| `token` | body | `string` | no | Access token when access_type=3. |
