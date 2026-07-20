# Create Note with Agile CRM

Creates a new note in Agile CRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/notes`
- **Base URL:** `https://mindcloud.agilecrm.com/dev/api`
- **Official documentation:** [Create Note](https://github.com/agilecrm/rest-api#41-create-a-note-and-relate-that-to-contacts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_ids[]` | body | `array<number>` | yes | Contact IDs for the note. Must be an array. |
| `subject` | body | `string` | no | Short note subject. |
| `description` | body | `string` | no | Note body content. |
