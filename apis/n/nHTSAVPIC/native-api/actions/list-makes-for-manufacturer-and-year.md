# List Makes for Manufacturer and Year with NHTSA vPIC

Retrieves makes for a manufacturer and year from NHTSA vPIC.

## Endpoint

- **Method:** `GET`
- **Path:** `vehicles/GetMakesForManufacturerAndYear/:manufacturer`
- **Base URL:** `https://vpic.nhtsa.dot.gov/api`
- **Official documentation:** [List Makes for Manufacturer and Year](https://vpic.nhtsa.dot.gov/api/Home/Index)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `manufacturer` | path | `string` | yes | Manufacturer name fragment or manufacturer ID. |
| `year` | query | `number` | yes | Model year that must fall within the make year range. |
