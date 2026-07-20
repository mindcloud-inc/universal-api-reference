# Get Contact with Constant Contact

Retrieves a contact from Constant Contact.

## Endpoint

- **Method:** `GET`
- **Path:** `/contacts/:contact_id`
- **Base URL:** `https://api.cc.email/v3`
- **Official documentation:** [Get Contact](https://developer.constantcontact.com/api_guide/contacts_get_one.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_id` | path | `string` | yes | Unique ID of the contact to retrieve. |
| `include` | query | `string` | no | Include contact sub-resources in the response. |
