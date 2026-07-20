# Update Departments with Odoo

Updates existing departments in Odoo.

## Endpoint

- **Method:** `POST`
- **Path:** `/hr.department/write`
- **Base URL:** `https://{domain}/json/2`
- **Official documentation:** [Update Departments](https://www.odoo.com/documentation/19.0/developer/reference/external_api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids[]` | body | `array<number>` | yes | Array of Odoo department IDs to update as JSON. |
| `vals` | body | `object` | yes | Object of department fields and values to update as JSON. |
