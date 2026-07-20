# Update Contact with CATS

Updates an existing contact in CATS.

## Endpoint

- **Method:** `PUT`
- **Path:** `/contacts/:id`
- **Base URL:** `https://api.catsone.com/v3`
- **Official documentation:** [Update Contact](https://docs.catsone.com/api/v3/#contacts-update-a-contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The ID of the contact to update. |
| `first_name` | body | `string` | yes | The contact first name. |
| `last_name` | body | `string` | yes | The contact last name. |
| `owner_id` | body | `number` | yes | The owning user ID. |
| `company_id` | body | `number` | yes | The company ID this contact belongs to. |
