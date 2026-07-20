# Update User with Dialpad

Updates an existing user in Dialpad.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/users/:id`
- **Base URL:** `https://dialpad.com/api/v2`
- **Official documentation:** [Update User](https://developers.dialpad.com/reference/usersupdate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The user's id. 'me' can be used if you are using a user level API key. |
| `first_name` | body | `string` | no | The user's first name. |
| `last_name` | body | `string` | no | The user's last name. |
| `emails[]` | body | `array<string>` | no | The user's emails. The first email in the list is the user's primary email. |
| `extension` | body | `string` | no | The user's new extension number. |
| `job_title` | body | `string` | no | The user's job title. |
| `license` | body | `string` | no | The user's license type. Changing this affects billing for the user. |
| `office_id` | body | `number` | no | The user's office id. |
| `admin_office_ids[]` | body | `array<number>` | no | The list of admin office IDs. |
| `phone_numbers[]` | body | `array<string>` | no | A list of the phone number(s) assigned to this user. |
| `forwarding_numbers[]` | body | `array<string>` | no | A list of phone numbers that should be dialed in addition to the user's Dialpad number(s) upon receiving a call. |
| `international_dialing_enabled` | body | `boolean` | no | Whether or not the user is enabled to dial internationally. |
| `is_super_admin` | body | `boolean` | no | Whether or not the user is a super admin. |
| `keep_paid_numbers` | body | `boolean` | no | Whether or not to keep phone numbers when switching to a support license. |
| `presence_status` | body | `object` | no | The presence status object to update. |
| `state` | body | `string` | no | The user's state. |
