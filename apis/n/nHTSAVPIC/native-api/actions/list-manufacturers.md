# List Manufacturers with NHTSA vPIC

Retrieves manufacturers from NHTSA vPIC.

## Endpoint

- **Method:** `GET`
- **Path:** `vehicles/GetAllManufacturers`
- **Base URL:** `https://vpic.nhtsa.dot.gov/api`
- **Official documentation:** [List Manufacturers](https://vpic.nhtsa.dot.gov/api/Home/Index)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ManufacturerType` | query | `string` | no | Optional manufacturer type name or partial name to narrow the manufacturer list. |
