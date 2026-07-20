# Add Note To Company with Datalyse

Adds a note to a company in Datalyse.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/1.0/companies/addnote.json`
- **Base URL:** `https://api.datalyse.io`
- **Official documentation:** [Add Note To Company](https://developers.datalyse.io/devs/content_api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_lead_id` | body | `string` | yes | ID of the company |
| `text` | body | `string` | yes | Text of the note |
