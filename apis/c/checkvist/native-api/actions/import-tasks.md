# Import Tasks with Checkvist

Imports tasks into a checklist in Checkvist.

## Endpoint

- **Method:** `POST`
- **Path:** `/checklists/:checklistId/import.json`
- **Base URL:** `https://checkvist.com`
- **Official documentation:** [Import Tasks](https://checkvist.com/auth/api#list_items_create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `checklistId` | path | `number` | yes | The checklist ID. |
| `import_content` | body | `string` | yes | The checklist content to import. |
| `import_content_note` | body | `string` | no | A note to attach to the first created task. |
| `parent_id` | body | `number` | no | The parent task ID. |
| `parse_tasks` | body | `boolean` | no | Recognize smart syntax in imported tasks. |
| `position` | body | `number` | no | The 1-based position for the first imported task. |
| `replace_existing` | body | `boolean` | no | Replace the existing checklist content. |
| `separate_with_empty_line` | body | `string` | no | Control how imported tasks are split. |
| `status` | body | `number` | no | The optional status for the first imported task. |
