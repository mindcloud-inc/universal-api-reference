# List Models for Make with NHTSA vPIC

Retrieves models for a make from NHTSA vPIC.

## Endpoint

- **Method:** `GET`
- **Path:** `vehicles/GetModelsForMake/:make`
- **Base URL:** `https://vpic.nhtsa.dot.gov/api`
- **Official documentation:** [List Models for Make](https://vpic.nhtsa.dot.gov/api/Home/Index)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `make` | path | `string` | yes | Make name fragment, such as honda. |
