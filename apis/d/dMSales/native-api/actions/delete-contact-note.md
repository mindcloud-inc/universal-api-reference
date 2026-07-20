# Delete Contact Note with DMSales

Deletes an existing contact note from DMSales.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/contact-card/delete-note`
- **Base URL:** `https://app.dmsales.com`
- **Official documentation:** [Delete Contact Note](https://app.dmsales.com/api-doc/default)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `base_key` | query | `string` | yes | Contact base key. |
| `note_id` | query | `string` | yes | Note UUID to delete. |
