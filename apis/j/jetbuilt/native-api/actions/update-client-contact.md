# Update Client Contact with Jetbuilt

Update a specified contact for a specified client.

## Endpoint

- **Method:** `PATCH`
- **Path:** `clients/:client_id/contacts/:contact_id`
- **Base URL:** `https://app.jetbuilt.com/api/`
- **Official documentation:** [Update Client Contact](https://api.jetbuilt.com/customers#update-a-client-contact)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `client_id` | path | `string` | no |
| `first_name` | body | `string` | no |
| `last_name` | body | `string` | no |
| `title` | body | `string` | no |
| `email_address` | body | `string` | no |
| `phone_number_1` | body | `string` | no |
| `phone_number_2` | body | `string` | no |
| `description` | body | `string` | no |
| `primary` | body | `boolean` | no |
| `contact_id` | path | `string` | no |
