# List Makes for Manufacturer with NHTSA vPIC

Retrieves makes for a manufacturer from NHTSA vPIC.

## Endpoint

- **Method:** `GET`
- **Path:** `vehicles/GetMakeForManufacturer/:manufacturer`
- **Base URL:** `https://vpic.nhtsa.dot.gov/api`
- **Official documentation:** [List Makes for Manufacturer](https://vpic.nhtsa.dot.gov/api/Home/Index)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `manufacturer` | path | `string` | yes | Manufacturer name fragment or manufacturer ID. |
