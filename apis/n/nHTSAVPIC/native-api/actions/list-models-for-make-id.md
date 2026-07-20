# List Models for Make ID with NHTSA vPIC

Retrieves models for a make ID from NHTSA vPIC.

## Endpoint

- **Method:** `GET`
- **Path:** `vehicles/GetModelsForMakeId/:makeId`
- **Base URL:** `https://vpic.nhtsa.dot.gov/api`
- **Official documentation:** [List Models for Make ID](https://vpic.nhtsa.dot.gov/api/Home/Index)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `makeId` | path | `number` | yes | Exact make ID from the vPIC dataset. |
