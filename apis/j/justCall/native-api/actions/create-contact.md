# Create Contact with JustCall

Creates a contact in JustCall.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2.1/contacts`
- **Base URL:** `https://api.justcall.io`
- **Official documentation:** [Create Contact](https://developer.justcall.io/reference/create_contact_v21)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company` | body | `string` | no | The contact's company name. |
| `contact_number` | body | `string` | yes | The contact's primary phone number. |
| `email` | body | `string` | no | The contact's email address. |
| `first_name` | body | `string` | yes | The contact's first name. |
| `last_name` | body | `string` | no | The contact's last name. |
