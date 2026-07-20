# Edit Contact Note with DMSales

Updates an existing contact note in DMSales.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/contact-card/edit-note`
- **Base URL:** `https://app.dmsales.com`
- **Official documentation:** [Edit Contact Note](https://app.dmsales.com/api-doc/default)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tag` | query | `string` | no | Optional note tag. |
| `base_key` | query | `string` | yes | Contact base key. |
| `note_id` | query | `string` | yes | Note UUID to edit. |
| `content` | query | `string` | yes | Updated note content. |
