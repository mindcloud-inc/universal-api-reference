# Update Contact with Sendblue

Updates an existing contact in Sendblue.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v2/contacts/:phone_number`
- **Base URL:** `https://api.sendblue.co`
- **Official documentation:** [Update Contact](https://docs.sendblue.com/api/resources/contacts/methods/update/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `phone_number` | path | `string` | yes | Phone number in E.164 format. |
| `first_name` | body | `string` | no | Contact's first name. |
| `last_name` | body | `string` | no | Contact's last name. |
| `company_name` | body | `string` | no | Company name. |
| `custom_variables` | body | `object` | no | Custom key-value pairs. Keys are human-readable labels; updates merge into the existing set. |
