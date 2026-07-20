# Add Contacts To List with Freshworks CRM

Adds contacts to a list in Freshworks CRM.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/lists/:id/add_contacts`
- **Base URL:** `https://{bundleAlias}`
- **Official documentation:** [Add Contacts To List](https://developers.freshworks.com/crm/api/#add_to_list)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `ids[]` | body | `array<number>` | yes |
