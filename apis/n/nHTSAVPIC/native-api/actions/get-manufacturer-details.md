# Get Manufacturer Details with NHTSA vPIC

Retrieves manufacturer details from NHTSA vPIC.

## Endpoint

- **Method:** `GET`
- **Path:** `vehicles/GetManufacturerDetails/:manufacturer`
- **Base URL:** `https://vpic.nhtsa.dot.gov/api`
- **Official documentation:** [Get Manufacturer Details](https://vpic.nhtsa.dot.gov/api/Home/Index)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `manufacturer` | path | `string` | yes | Manufacturer name fragment or manufacturer ID. |
