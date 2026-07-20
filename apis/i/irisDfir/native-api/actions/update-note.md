# Update Note with Iris Dfir

## Endpoint

- **Method:** `POST`
- **Path:** `/case/notes/update/:identifier`
- **Base URL:** `https://v200.beta.dfir-iris.org`
- **Official documentation:** [Update Note](https://docs.dfir-iris.org/2.4.20/_static/iris_api_reference_v2.0.4.html#tag/Case-notes/operation/case_notes_update_(note_id)_post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifier` | path | `number` | yes | IRIS note identifier. |
| `directory_id` | body | `number` | yes | Directory id to keep or move the note under. |
| `note_title` | body | `string` | yes | Updated note title. |
| `note_content` | body | `string` | yes | Updated note content. |
