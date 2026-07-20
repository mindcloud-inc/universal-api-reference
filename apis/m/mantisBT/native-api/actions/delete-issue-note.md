# Delete Issue Note with MantisBT

Deletes an issue note from MantisBT.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/issues/{issue_id}/notes/{issue_note_id}`
- **Base URL:** `{baseUrl}/api/rest`
- **Official documentation:** [Delete Issue Note](https://github.com/mantisbt/mantisbt/blob/release-2.28.0/api/rest/mantisbt_openapi.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `issue_id` | path | `number` | yes | ID of the issue that owns the note |
| `issue_note_id` | path | `number` | yes | ID of the note to delete |
| `text` | body | `string` | yes | Text of the note being deleted |
