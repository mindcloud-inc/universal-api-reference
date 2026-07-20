# Register Conference Participant with ClickMeeting

Creates a conference participant registration in ClickMeeting.

## Endpoint

- **Method:** `POST`
- **Path:** `conferences/{{room_id}}/registration`
- **Base URL:** `https://api.clickmeeting.com/v1`
- **Official documentation:** [Register Conference Participant](https://dev.clickmeeting.com/api-doc/#post_registration)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `room_id` | path | `number` | yes | Conference room identifier. |
| `first_name` | body | `string` | yes | Participant first name. |
| `last_name` | body | `string` | yes | Participant last name. |
| `email` | body | `string` | yes | Participant email address. |
| `confirmation_email_enabled` | body | `boolean` | no | Enable ClickMeeting confirmation email delivery. |
| `confirmation_email_lang` | body | `string` | no | Confirmation email language token. |
