# List WMIs for Manufacturer with NHTSA vPIC

Retrieves WMIs for a manufacturer from NHTSA vPIC.

## Endpoint

- **Method:** `GET`
- **Path:** `vehicles/GetWMIsForManufacturer/:manufacturer`
- **Base URL:** `https://vpic.nhtsa.dot.gov/api`
- **Official documentation:** [List WMIs for Manufacturer](https://vpic.nhtsa.dot.gov/api/Home/Index)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `manufacturer` | path | `string` | no | A manufacturer ID or a full or partial manufacturer name. |
| `manufacturer` | path | `string` | yes | Manufacturer name fragment or manufacturer ID. |
| `vehicleType` | query | `string` | no | Optional vehicle type ID or full or partial vehicle type name to narrow the WMI results. |
| `vehicleType` | query | `string` | no | Optional vehicle type name fragment or vehicle type ID to narrow the WMI list. |
