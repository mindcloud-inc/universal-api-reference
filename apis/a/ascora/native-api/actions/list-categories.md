# List Categories with Ascora

Retrieves categories from Ascora.

## Endpoint

- **Method:** `GET`
- **Path:** `/Inventory/Categories`
- **Base URL:** `https://api.ascora.com.au`
- **Official documentation:** [List Categories](https://www.dropbox.com/scl/fi/75586ygs35arfb7d3cvxi/API-Endpoints-1.2.pdf?rlkey=ztci7pf4nuasegnybjreqsqe2&dl=0#page=19)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `FilterText` | query | `string` | no | Search across the category name. |
| `ParentOnly` | query | `boolean` | no | Return top-level categories only. |
| `CategoryNumber` | query | `number` | no | Filter to category group 1 or 2. |
