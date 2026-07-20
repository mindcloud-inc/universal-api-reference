# Update Job Positions with Odoo

Updates existing job positions in Odoo.

## Endpoint

- **Method:** `POST`
- **Path:** `/hr.job/write`
- **Base URL:** `https://{domain}/json/2`
- **Official documentation:** [Update Job Positions](https://www.odoo.com/documentation/19.0/developer/reference/external_api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids[]` | body | `array<number>` | yes | Array of Odoo job position IDs to update as JSON. |
| `vals` | body | `object` | yes | Object of job position fields and values to update as JSON. |
