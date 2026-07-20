# Create Contact with CATS

Creates a new contact in CATS.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts`
- **Base URL:** `https://api.catsone.com/v3`
- **Official documentation:** [Create Contact](https://docs.catsone.com/api/v3/#contacts-create-a-contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `first_name` | body | `string` | yes | The contact first name. |
| `last_name` | body | `string` | yes | The contact last name. |
| `owner_id` | body | `number` | yes | The owning user ID. |
| `company_id` | body | `number` | yes | The company ID this contact belongs to. |
| `check_duplicate` | query | `boolean` | no | Throw an error instead of creating a duplicate when true. |
