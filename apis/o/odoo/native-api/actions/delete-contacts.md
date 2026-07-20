# Delete Contacts with Odoo

Deletes contacts from Odoo.

## Endpoint

- **Method:** `POST`
- **Path:** `/res.partner/unlink`
- **Base URL:** `https://{domain}/json/2`
- **Official documentation:** [Delete Contacts](https://www.odoo.com/documentation/19.0/developer/reference/external_api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids[]` | body | `array<number>` | yes | Array of Odoo record IDs to delete as JSON. |
