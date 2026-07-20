# List Models for Make ID and Year with NHTSA vPIC

Retrieves models for a make ID and year from NHTSA vPIC.

## Endpoint

- **Method:** `GET`
- **Path:** `vehicles/GetModelsForMakeIdYear/makeId/:makeId/modelyear/:modelYear`
- **Base URL:** `https://vpic.nhtsa.dot.gov/api`
- **Official documentation:** [List Models for Make ID and Year](https://vpic.nhtsa.dot.gov/api/Home/Index)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `makeId` | path | `number` | yes | Exact make ID from the vPIC dataset. |
| `modelYear` | path | `number` | yes | Model year greater than 1995. |
