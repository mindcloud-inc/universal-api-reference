# Create Contact with Insightly

Creates a new contact in Insightly.

## Endpoint

- **Method:** `POST`
- **Path:** `{apiBaseUrl}Contacts`
- **Base URL:** `https://api.na1.insightly.com/v3.1/`
- **Official documentation:** [Create Contact](https://api.insightly.com/v3.1/Help#!/Contacts/AddEntity)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `FIRST_NAME` | body | `string` | yes | The contact's first name. |
| `LAST_NAME` | body | `string` | no | The contact's last name. |
| `EMAIL_ADDRESS` | body | `string` | no | The contact's email address. |
| `PHONE` | body | `string` | no | The contact's primary phone number. |
| `TITLE` | body | `string` | no | The contact's job title. |
| `ORGANISATION_ID` | body | `number` | no | The related Organisation ID. |
