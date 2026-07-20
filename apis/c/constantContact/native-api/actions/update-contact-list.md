# Update Contact List with Constant Contact

Updates a contact list in Constant Contact.

## Endpoint

- **Method:** `PUT`
- **Path:** `/contact_lists/:list_id`
- **Base URL:** `https://api.cc.email/v3`
- **Official documentation:** [Update Contact List](https://developer.constantcontact.com/api_guide/lists_put.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `list_id` | path | `string` | yes | Unique ID of the contact list to update. |
| `name` | body | `string` | yes | Updated contact list name. |
| `favorite` | body | `boolean` | no | Whether to mark the list as favorite. |
| `description` | body | `string` | no | Updated list description. |
