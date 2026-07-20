# Create To Do with Cloze

Creates a to-do in Cloze.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/timeline/todo/create`
- **Base URL:** `https://api.cloze.com`
- **Official documentation:** [Create To Do](https://api.cloze.com/api-docs/#/paths/v1-timeline-todo-create/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subject` | body | `string` | no | Subject or description for this To Do. |
| `when` | body | `string` | no | Reminder date/time or someday marker. |
| `participants[]` | body | `array<string>` | no | People or companies related to the To Do. |
| `assignee` | body | `string` | no | Cloze user this To Do is assigned to. |
