# Create Departments with Odoo

Creates new departments in Odoo.

## Endpoint

- **Method:** `POST`
- **Path:** `/hr.department/create`
- **Base URL:** `https://{domain}/json/2`
- **Official documentation:** [Create Departments](https://www.odoo.com/documentation/19.0/developer/reference/external_api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `vals_list[]` | body | `array<object>` | yes | Array of department objects to create as JSON. |
