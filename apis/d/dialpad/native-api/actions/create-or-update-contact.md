# Create or Update Contact with Dialpad

Creates or updates a contact in Dialpad by unique ID.

## Endpoint

- **Method:** `PUT`
- **Path:** `/contacts`
- **Base URL:** `https://dialpad.com/api/v2`
- **Official documentation:** [Create or Update Contact](https://developers.dialpad.com/reference/contactscreate_with_uid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_name` | body | `string` | no | The contact's company name. |
| `emails[]` | body | `array<string>` | no | The contact's emails. The first email in the list is the contact's primary email. |
| `extension` | body | `string` | no | The contact's extension number. |
| `first_name` | body | `string` | yes | The contact's first name. |
| `job_title` | body | `string` | no | The contact's job title. |
| `last_name` | body | `string` | yes | The contact's last name. |
| `phones[]` | body | `array<string>` | no | The contact's phone numbers. The first number in the list is the contact's primary phone. |
| `uid` | body | `string` | yes | The unique id to be included as part of the contact's generated id. |
| `urls[]` | body | `array<string>` | no | A list of websites associated with or belonging to this contact. |
