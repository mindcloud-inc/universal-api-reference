# Get Contacts By IDs with Odoo

Retrieves contacts by ID from Odoo.

## Endpoint

- **Method:** `POST`
- **Path:** `/res.partner/read`
- **Base URL:** `https://{domain}/json/2`
- **Official documentation:** [Get Contacts By IDs](https://www.odoo.com/documentation/19.0/developer/reference/external_api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fields[]` | body | `array<string>` | no | Optional array of field names to include. |
| `ids[]` | body | `array<number>` | yes | Array of Odoo record IDs to read as JSON. |
