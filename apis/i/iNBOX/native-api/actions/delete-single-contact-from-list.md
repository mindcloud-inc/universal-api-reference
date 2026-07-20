# Delete Single Contact From List with INBOX

Removes a contact from an INBOX contact list.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/inbox/v1/contactlists/:id/delete/:contact-id`
- **Base URL:** `https://useapi.useinbox.com`
- **Official documentation:** [Delete Single Contact From List](https://reference.useinbox.com/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `contact-id` | path | `string` | yes |
| `id` | path | `string` | yes |
