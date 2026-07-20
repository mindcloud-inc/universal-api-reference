# List Vehicle Types for Make ID with NHTSA vPIC

Retrieves vehicle types for a make ID from NHTSA vPIC.

## Endpoint

- **Method:** `GET`
- **Path:** `vehicles/GetVehicleTypesForMakeId/:makeId`
- **Base URL:** `https://vpic.nhtsa.dot.gov/api`
- **Official documentation:** [List Vehicle Types for Make ID](https://vpic.nhtsa.dot.gov/api/Home/Index)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `makeId` | path | `number` | yes | Exact make ID from the vPIC dataset. |
