# Get Departments By IDs with Odoo

Retrieves departments by ID from Odoo.

## Endpoint

- **Method:** `POST`
- **Path:** `/hr.department/read`
- **Base URL:** `https://{domain}/json/2`
- **Official documentation:** [Get Departments By IDs](https://www.odoo.com/documentation/19.0/developer/reference/external_api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fields[]` | body | `array<string>` | no | Optional array of department field names to include. |
| `ids[]` | body | `array<number>` | yes | Array of Odoo department IDs to read as JSON. |
