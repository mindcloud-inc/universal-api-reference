# Add Note To Lead with Datalyse

Adds a note to a contact or company in Datalyse.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/1.0/leads/addnote.json`
- **Base URL:** `https://api.datalyse.io`
- **Official documentation:** [Add Note To Lead](https://developers.datalyse.io/devs/content_api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lead_id` | body | `string` | yes | ID of the contact or company |
| `text` | body | `string` | yes | Text of the note |
