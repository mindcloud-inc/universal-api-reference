# List Vehicle Types for Make with NHTSA vPIC

Retrieves vehicle types for a make from NHTSA vPIC.

## Endpoint

- **Method:** `GET`
- **Path:** `vehicles/GetVehicleTypesForMake/:make`
- **Base URL:** `https://vpic.nhtsa.dot.gov/api`
- **Official documentation:** [List Vehicle Types for Make](https://vpic.nhtsa.dot.gov/api/Home/Index)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `make` | path | `string` | yes | Make name fragment, such as mercedes. |
