# Move Contacts Between Lists with Freshworks CRM

Moves contacts between lists in Freshworks CRM.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/lists/:id/move_contacts`
- **Base URL:** `https://{bundleAlias}`
- **Official documentation:** [Move Contacts Between Lists](https://developers.freshworks.com/crm/api/#move_contact_from_list)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `all` | body | `boolean` | no |
| `from_list_id` | body | `number` | yes |
| `id` | path | `string` | yes |
| `ids[]` | body | `array<number>` | no |
