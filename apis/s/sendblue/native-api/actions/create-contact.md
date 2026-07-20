# Create Contact with Sendblue

Creates a new contact in Sendblue.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/contacts`
- **Base URL:** `https://api.sendblue.co`
- **Official documentation:** [Create Contact](https://docs.sendblue.com/api/resources/contacts/methods/create/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `number` | body | `string` | yes | Phone number in E.164 format. |
| `first_name` | body | `string` | no | Contact's first name. |
| `last_name` | body | `string` | no | Contact's last name. |
| `company_name` | body | `string` | no | Company name. |
| `custom_variables` | body | `object` | no | Custom key-value pairs. Keys are human-readable labels; new labels are auto-created. |
| `update_if_exists` | body | `boolean` | no | Update the existing contact if the phone number already exists. |
