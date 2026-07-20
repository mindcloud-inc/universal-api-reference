# Delete Job Positions with Odoo

Deletes job positions from Odoo.

## Endpoint

- **Method:** `POST`
- **Path:** `/hr.job/unlink`
- **Base URL:** `https://{domain}/json/2`
- **Official documentation:** [Delete Job Positions](https://www.odoo.com/documentation/19.0/developer/reference/external_api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids[]` | body | `array<number>` | yes | Array of Odoo job position IDs to delete as JSON. |
