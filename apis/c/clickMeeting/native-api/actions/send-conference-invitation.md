# Send Conference Invitation with ClickMeeting

Sends a conference invitation email from ClickMeeting.

## Endpoint

- **Method:** `POST`
- **Path:** `conferences/{{room_id}}/invitation/email/{{lang}}`
- **Base URL:** `https://api.clickmeeting.com/v1`
- **Official documentation:** [Send Conference Invitation](https://dev.clickmeeting.com/api-doc/#post_invite_email)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `room_id` | path | `number` | yes | Conference room identifier. |
| `lang` | path | `string` | yes | Invitation language token from ClickMeeting. |
| `attendee_emails` | body | `string` | yes | One or more attendee email addresses. Send multiple values as a array separated by `,`. |
| `template` | body | `list` | no | Invitation template style. Accepted values: `advanced`, `basic`. |
| `role` | body | `list` | no | Invitation recipient role. Accepted values: `listener`, `presenter`. |
