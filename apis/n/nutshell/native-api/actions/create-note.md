# Create Note with Nutshell

Creates a new note in Nutshell.

## Endpoint

- **Method:** `POST`
- **Path:** `/notes`
- **Base URL:** `https://app.nutshell.com/rest`
- **Official documentation:** [Create Note](https://developers.nutshell.com/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data.body` | body | `string` | no | Text to display in the note. |
| `data.links.parent` | body | `string` | no | Entity ID to attach the note to. |
