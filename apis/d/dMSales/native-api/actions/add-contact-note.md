# Add Contact Note with DMSales

Creates a contact note in DMSales.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/contact-card/add-note`
- **Base URL:** `https://app.dmsales.com`
- **Official documentation:** [Add Contact Note](https://app.dmsales.com/api-doc/default)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `base_key` | query | `string` | yes | Contact base key. |
| `content` | query | `string` | yes | Note content. |
| `tag` | query | `string` | no | Optional note tag. |
