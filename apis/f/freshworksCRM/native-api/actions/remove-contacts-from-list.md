# Remove Contacts From List with Freshworks CRM

Removes contacts from a list in Freshworks CRM.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/lists/:id/remove_contacts`
- **Base URL:** `https://{bundleAlias}`
- **Official documentation:** [Remove Contacts From List](https://developers.freshworks.com/crm/api/#remove_contact_from_list)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `all` | body | `boolean` | no |
| `id` | path | `string` | yes |
| `ids[]` | body | `array<number>` | no |
