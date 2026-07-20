# Create Contact with Zoho FSM

Creates a new contact in Zoho FSM.

## Endpoint

- **Method:** `POST`
- **Path:** `/Contacts`
- **Base URL:** `{api_domain}/fsm/v1`
- **Official documentation:** [Create Contact](https://www.zoho.com/fsm/developer/help/api/create-contact.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data[]` | body | `string` | no | — |
| `data[0].Last_Name` | body | `string` | yes | The last name of the contact. |
| `data[0].Email` | body | `string` | yes | The email address to associate with the contact. |
