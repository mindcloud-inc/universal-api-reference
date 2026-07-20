# Delete Departments with Odoo

Deletes departments from Odoo.

## Endpoint

- **Method:** `POST`
- **Path:** `/hr.department/unlink`
- **Base URL:** `https://{domain}/json/2`
- **Official documentation:** [Delete Departments](https://www.odoo.com/documentation/19.0/developer/reference/external_api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids[]` | body | `array<number>` | yes | Array of Odoo department IDs to delete as JSON. |
