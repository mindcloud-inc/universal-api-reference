# Add Note To Task with Datalyse

Adds a note to a task in Datalyse.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/1.0/tasks/addnote.json`
- **Base URL:** `https://api.datalyse.io`
- **Official documentation:** [Add Note To Task](https://developers.datalyse.io/devs/content_api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `task_id` | body | `string` | yes | ID of the task |
| `text` | body | `string` | yes | Text of the note |
