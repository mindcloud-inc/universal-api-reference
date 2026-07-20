# Create Or Update Contact with GetSales.io

## Endpoint

- **Method:** `POST`
- **Path:** `/leads/api/leads/upsert`
- **Base URL:** `https://amazing.getsales.io`
- **Official documentation:** [Create Or Update Contact](https://api.getsales.io/api/openapi/contacts/upsertcontact.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lead.linkedin_id` | body | `string` | yes | Contact LinkedIn ID or profile handle. |
| `lead.email` | body | `string` | no | Contact email address. |
| `lead.first_name` | body | `string` | no | Contact first name. |
| `lead.last_name` | body | `string` | no | Contact last name. |
| `lead.company_name` | body | `string` | no | Contact company name. |
| `list_uuid` | body | `string` | yes | UUID of the target list. |
| `update_if_exists` | body | `boolean` | no | When true, updates the contact if it already exists. |
| `move_to_list` | body | `boolean` | no | When true, moves an existing contact to the specified list. |
