# Clone Contact with Freshworks CRM

Creates a contact by cloning one in Freshworks CRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/contacts/:id/clone`
- **Base URL:** `https://{bundleAlias}`
- **Official documentation:** [Clone Contact](https://developers.freshworks.com/crm/api/#clone_a_contact)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `contact` | body | `string` | no |
| `id` | path | `string` | yes |
