# Create Contact List with Constant Contact

Creates a contact list in Constant Contact.

## Endpoint

- **Method:** `POST`
- **Path:** `/contact_lists`
- **Base URL:** `https://api.cc.email/v3`
- **Official documentation:** [Create Contact List](https://developer.constantcontact.com/api_guide/lists_post.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Contact list name. |
| `favorite` | body | `boolean` | no | Whether to mark the list as favorite. |
| `description` | body | `string` | no | List description. |
