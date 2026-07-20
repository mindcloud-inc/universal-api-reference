# Update Note with Freshworks CRM

Updates an existing note in Freshworks CRM.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/notes/:id`
- **Base URL:** `https://{bundleAlias}`
- **Official documentation:** [Update Note](https://developers.freshworks.com/crm/api/#update_note)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `note` | body | `object` | yes |
| `note.description` | body | `string` | yes |
| `note.targetable_id` | body | `number` | yes |
| `note.targetable_type` | body | `string` | yes |
