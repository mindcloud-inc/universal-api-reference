# Create Contacts with Odoo

Creates new contacts in Odoo.

## Endpoint

- **Method:** `POST`
- **Path:** `/res.partner/create`
- **Base URL:** `https://{domain}/json/2`
- **Official documentation:** [Create Contacts](https://www.odoo.com/documentation/19.0/developer/reference/external_api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `vals_list[]` | body | `array<object>` | yes | Array of objects to create as JSON. |
