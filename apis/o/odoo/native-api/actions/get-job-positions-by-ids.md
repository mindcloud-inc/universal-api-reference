# Get Job Positions By IDs with Odoo

Retrieves job positions by ID from Odoo.

## Endpoint

- **Method:** `POST`
- **Path:** `/hr.job/read`
- **Base URL:** `https://{domain}/json/2`
- **Official documentation:** [Get Job Positions By IDs](https://www.odoo.com/documentation/19.0/developer/reference/external_api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fields[]` | body | `array<string>` | no | Optional array of job position field names to include. |
| `ids[]` | body | `array<number>` | yes | Array of Odoo job position IDs to read as JSON. |
