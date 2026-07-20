# Update Contacts with Odoo

Updates existing contacts in Odoo.

## Endpoint

- **Method:** `POST`
- **Path:** `/res.partner/write`
- **Base URL:** `https://{domain}/json/2`
- **Official documentation:** [Update Contacts](https://www.odoo.com/documentation/19.0/developer/reference/external_api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids[]` | body | `array<number>` | yes | Array of Odoo record IDs to update as JSON. |
| `vals` | body | `object` | yes | Object of fields and values to update as JSON. |
