# Create Note with Edoobox

Creates a new note in Edoobox.

## Endpoint

- **Method:** `POST`
- **Path:** `/note`
- **Base URL:** `https://app2.edoobox.com/v2`
- **Official documentation:** [Create Note](https://api.docs.edoobox.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subject` | body | `string` | yes | Note subject. |
| `message` | body | `string` | yes | Note message body. |
| `todo` | body | `boolean` | no | Whether the note is a TODO item. |
| `type` | body | `string` | no | edoobox note type. |
