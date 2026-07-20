# Create Job Positions with Odoo

Creates new job positions in Odoo.

## Endpoint

- **Method:** `POST`
- **Path:** `/hr.job/create`
- **Base URL:** `https://{domain}/json/2`
- **Official documentation:** [Create Job Positions](https://www.odoo.com/documentation/19.0/developer/reference/external_api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `vals_list[]` | body | `array<object>` | yes | Array of job position objects to create as JSON. |
