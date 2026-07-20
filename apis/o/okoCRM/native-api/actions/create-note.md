# Create note with OkoCRM

Creates a new note in OkoCRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/notes/note`
- **Base URL:** `https://api.okocrm.com/v2`
- **Official documentation:** [Create note](https://okocrm.com/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_id` | body | `number` | yes | Attach the note to a contact. |
| `text` | body | `string` | yes | Note text. |
