# NHTSA vPIC: Native API Reference

A consolidated summary of NHTSA vPIC's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://vpic.nhtsa.dot.gov/api/Home/Index
- **API base URL:** `https://vpic.nhtsa.dot.gov/api`

## Authentication

### No Authentication

Public API; no credentials or registration required.

This API does not require request authentication.

[Official authentication documentation](https://vpic.nhtsa.dot.gov/api/Home/Index/FAQ)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `Results`.

## Pagination

Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Decode VIN](actions/decode-vin.md) | `GET vehicles/DecodeVin/:vin` | [docs](https://vpic.nhtsa.dot.gov/api/Home/Index) |
| [Decode VIN Extended](actions/decode-vin-extended.md) | `GET vehicles/DecodeVinExtended/:vin` | [docs](https://vpic.nhtsa.dot.gov/api/Home/Index) |
| [Decode VIN Values](actions/decode-vin-values.md) | `GET vehicles/DecodeVinValues/:vin` | [docs](https://vpic.nhtsa.dot.gov/api/Home/Index) |
| [Decode VIN Values Extended](actions/decode-vin-values-extended.md) | `GET vehicles/DecodeVinValuesExtended/:vin` | [docs](https://vpic.nhtsa.dot.gov/api/Home/Index) |
| [Decode WMI](actions/decode-wmi.md) | `GET vehicles/DecodeWMI/:wmi` | [docs](https://vpic.nhtsa.dot.gov/api/Home/Index) |
| [Get Manufacturer Details](actions/get-manufacturer-details.md) | `GET vehicles/GetManufacturerDetails/:manufacturer` | [docs](https://vpic.nhtsa.dot.gov/api/Home/Index) |
| [List Makes](actions/list-makes.md) | `GET vehicles/GetAllMakes` | [docs](https://vpic.nhtsa.dot.gov/api/Home/Index) |
| [List Makes for Manufacturer](actions/list-makes-for-manufacturer.md) | `GET vehicles/GetMakeForManufacturer/:manufacturer` | [docs](https://vpic.nhtsa.dot.gov/api/Home/Index) |
| [List Makes for Manufacturer and Year](actions/list-makes-for-manufacturer-and-year.md) | `GET vehicles/GetMakesForManufacturerAndYear/:manufacturer` | [docs](https://vpic.nhtsa.dot.gov/api/Home/Index) |
| [List Makes for Vehicle Type](actions/list-makes-for-vehicle-type.md) | `GET vehicles/GetMakesForVehicleType/:vehicleType` | [docs](https://vpic.nhtsa.dot.gov/api/Home/Index) |
| [List Manufacturers](actions/list-manufacturers.md) | `GET vehicles/GetAllManufacturers` | [docs](https://vpic.nhtsa.dot.gov/api/Home/Index) |
| [List Models for Make](actions/list-models-for-make.md) | `GET vehicles/GetModelsForMake/:make` | [docs](https://vpic.nhtsa.dot.gov/api/Home/Index) |
| [List Models for Make and Year](actions/list-models-for-make-and-year.md) | `GET vehicles/GetModelsForMakeYear/make/:make/modelyear/:modelYear` | [docs](https://vpic.nhtsa.dot.gov/api/Home/Index) |
| [List Models for Make ID](actions/list-models-for-make-id.md) | `GET vehicles/GetModelsForMakeId/:makeId` | [docs](https://vpic.nhtsa.dot.gov/api/Home/Index) |
| [List Models for Make ID and Year](actions/list-models-for-make-id-and-year.md) | `GET vehicles/GetModelsForMakeIdYear/makeId/:makeId/modelyear/:modelYear` | [docs](https://vpic.nhtsa.dot.gov/api/Home/Index) |
| [List Vehicle Types for Make](actions/list-vehicle-types-for-make.md) | `GET vehicles/GetVehicleTypesForMake/:make` | [docs](https://vpic.nhtsa.dot.gov/api/Home/Index) |
| [List Vehicle Types for Make ID](actions/list-vehicle-types-for-make-id.md) | `GET vehicles/GetVehicleTypesForMakeId/:makeId` | [docs](https://vpic.nhtsa.dot.gov/api/Home/Index) |
| [List Vehicle Variable Values](actions/list-vehicle-variable-values.md) | `GET vehicles/GetVehicleVariableValuesList/:variable` | [docs](https://vpic.nhtsa.dot.gov/api/Home/Index) |
| [List Vehicle Variables](actions/list-vehicle-variables.md) | `GET vehicles/GetVehicleVariableList` | [docs](https://vpic.nhtsa.dot.gov/api/Home/Index) |
| [List WMIs for Manufacturer](actions/list-wmis-for-manufacturer.md) | `GET vehicles/GetWMIsForManufacturer/:manufacturer` | [docs](https://vpic.nhtsa.dot.gov/api/Home/Index) |
