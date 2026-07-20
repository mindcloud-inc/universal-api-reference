# Create Contact with Dialpad

Creates a new contact in Dialpad.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts`
- **Base URL:** `https://dialpad.com/api/v2`
- **Official documentation:** [Create Contact](https://developers.dialpad.com/reference/contactscreate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_name` | body | `string` | no | The contact's company name. |
| `emails[]` | body | `array<string>` | no | The contact's emails. The first email in the list is the contact's primary email. |
| `extension` | body | `string` | no | The contact's extension number. |
| `first_name` | body | `string` | yes | The contact's first name. |
| `job_title` | body | `string` | no | The contact's job title. |
| `last_name` | body | `string` | yes | The contact's last name. |
| `owner_id` | body | `string` | no | If provided, a local contact will be created for this user. |
| `phones[]` | body | `array<string>` | no | The contact's phone numbers. The first number in the list is the contact's primary phone. |
| `urls[]` | body | `array<string>` | no | A list of websites associated with or belonging to this contact. |
