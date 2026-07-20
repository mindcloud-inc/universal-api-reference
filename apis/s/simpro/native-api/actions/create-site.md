# Create Site with Simpro

## Endpoint

- **Method:** `POST`
- **Path:** `/companies/:companyId/sites/`
- **Base URL:** `https://mindcloud.simprosuite.com/api/v1.0`
- **Official documentation:** [Create Site](https://developer.simprogroup.com/apidoc/?page=3faa64303d5f5bcd043bb88f6768e603)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyId` | path | `number` | yes | Simpro company ID. Single-company builds usually use 0. |
| `Name` | body | `string` | yes | Site name. |
| `Customers[]` | body | `array<number>` | no | Customer IDs linked to the site. |
