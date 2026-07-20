# Add Note To Opportunity with Datalyse

Adds a note to an opportunity in Datalyse.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/1.0/opportunities/addnote.json`
- **Base URL:** `https://api.datalyse.io`
- **Official documentation:** [Add Note To Opportunity](https://developers.datalyse.io/devs/content_api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `opportunity_id` | body | `string` | yes | ID of the opportunity |
| `text` | body | `string` | yes | Text of the note |
