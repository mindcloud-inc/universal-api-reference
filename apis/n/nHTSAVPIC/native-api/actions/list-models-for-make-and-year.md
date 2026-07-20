# List Models for Make and Year with NHTSA vPIC

Retrieves models for a make and year from NHTSA vPIC.

## Endpoint

- **Method:** `GET`
- **Path:** `vehicles/GetModelsForMakeYear/make/:make/modelyear/:modelYear`
- **Base URL:** `https://vpic.nhtsa.dot.gov/api`
- **Official documentation:** [List Models for Make and Year](https://vpic.nhtsa.dot.gov/api/Home/Index)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `make` | path | `string` | yes | Make name fragment, such as honda. |
| `modelYear` | path | `number` | yes | Model year greater than 1995. |
