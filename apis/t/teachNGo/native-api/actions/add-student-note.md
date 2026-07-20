# Add Student Note with Teach 'n Go

Creates a student note in Teach 'n Go.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/note/add`
- **Base URL:** `https://app.teachngo.com`
- **Official documentation:** [Add Student Note](https://intercom.help/teach-n-go/en/articles/9123701-add-a-student-note-using-the-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `student_id` | body | `string` | yes | The student record that should receive the note. |
| `visibility` | body | `string` | yes | Set to public or private. |
| `note` | body | `string` | yes | The note content to add to the student record. |
