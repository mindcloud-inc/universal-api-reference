# List Makes for Vehicle Type with NHTSA vPIC

Retrieves makes for a vehicle type from NHTSA vPIC.

## Endpoint

- **Method:** `GET`
- **Path:** `vehicles/GetMakesForVehicleType/:vehicleType`
- **Base URL:** `https://vpic.nhtsa.dot.gov/api`
- **Official documentation:** [List Makes for Vehicle Type](https://vpic.nhtsa.dot.gov/api/Home/Index)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `vehicleType` | path | `string` | yes | Vehicle type name fragment, such as car or motorcycle. |
