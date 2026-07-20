# List Vehicle Variable Values with NHTSA vPIC

Retrieves vehicle variable values from NHTSA vPIC.

## Endpoint

- **Method:** `GET`
- **Path:** `vehicles/GetVehicleVariableValuesList/:variable`
- **Base URL:** `https://vpic.nhtsa.dot.gov/api`
- **Official documentation:** [List Vehicle Variable Values](https://vpic.nhtsa.dot.gov/api/Home/Index)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variable` | path | `string` | yes | Full vehicle variable name or exact variable ID. |
