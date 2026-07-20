# Create Note with Freshworks CRM

Creates a new note in Freshworks CRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/notes`
- **Base URL:** `https://{bundleAlias}`
- **Official documentation:** [Create Note](https://developers.freshworks.com/crm/api/#create_note)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `note` | body | `object` | yes |
| `note.description` | body | `string` | yes |
| `note.targetable_id` | body | `number` | yes |
| `note.targetable_type` | body | `string` | yes |
