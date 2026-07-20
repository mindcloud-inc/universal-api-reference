# Update Contact with PhoneBurner

Updates an existing contact in PhoneBurner.

## Endpoint

- **Method:** `PUT`
- **Path:** `rest/1/contacts/{{contactId}}`
- **Base URL:** `https://www.phoneburner.com/`
- **Official documentation:** [Update Contact](https://www.phoneburner.com/developer/route_list#contacts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactId` | path | `string` | no | The PhoneBurner contact id. |
| `email` | body | `string` | no | Updated email address. |
| `first_name` | body | `string` | no | Updated first name. |
| `last_name` | body | `string` | no | Updated last name. |
| `notes` | body | `string` | no | Updated notes. |
| `phone` | body | `string` | no | Updated phone number. |
