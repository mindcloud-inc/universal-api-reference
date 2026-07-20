# Update Contact with Dialpad

Updates an existing contact in Dialpad.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/contacts/:id`
- **Base URL:** `https://dialpad.com/api/v2`
- **Official documentation:** [Update Contact](https://developers.dialpad.com/reference/contactsupdate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The contact's id. |
| `company_name` | body | `string` | no | The contact's company name. |
| `emails[]` | body | `array<string>` | no | The contact's emails. The first email in the list is the contact's primary email. |
| `extension` | body | `string` | no | The contact's extension number. |
| `first_name` | body | `string` | no | The contact's first name. |
| `job_title` | body | `string` | no | The contact's job title. |
| `last_name` | body | `string` | no | The contact's last name. |
| `phones[]` | body | `array<string>` | no | The contact's phone numbers. The first number in the list is the contact's primary phone. |
| `urls[]` | body | `array<string>` | no | A list of websites associated with or belonging to this contact. |
