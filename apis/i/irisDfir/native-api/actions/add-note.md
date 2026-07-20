# Add Note with Iris Dfir

## Endpoint

- **Method:** `POST`
- **Path:** `/case/notes/add`
- **Base URL:** `https://v200.beta.dfir-iris.org`
- **Official documentation:** [Add Note](https://docs.dfir-iris.org/2.4.20/_static/iris_api_reference_v2.0.4.html#tag/Case-notes/operation/case_notes_add_post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `directory_id` | body | `number` | yes | IRIS note directory identifier. |
| `note_title` | body | `string` | yes | Title of the note. |
| `note_content` | body | `string` | yes | Content of the note. |
