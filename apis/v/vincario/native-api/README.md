# Vincario: Native API Reference

A consolidated summary of Vincario's API configuration and 15 documented operations, with links to official documentation.

- **Official docs:** https://vincario.com/api-docs/3.2/
- **OpenAPI specification:** https://vincario.com/api-docs/openapi/3.2
- **API base URL:** `https://api.vincario.com/3.2`

## Authentication

### API Key + Secret Signature

Use your Vincario API key and secret key to sign each request.

### Credentials

- **API Key:** `apiKey` · required · Your Vincario API key.
- **Secret Key:** `secretKey` · required · Your Vincario secret key used to calculate the control sum.

[Official authentication documentation](https://vincario.com/api-docs/3.2/#api-how-to-create-a-request)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (15 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Balance](actions/get-balance.md) | `GET /:apiKey/:controlSum/balance.:format` | [docs](https://vincario.com/api-docs/3.2/#operations-Get_Balance-Get_Balance) |
| [List Body Types](actions/list-body-types.md) | `GET /:apiKey/:controlSum/decode/value-list/enum/enum_body.:format` | [docs](https://vincario.com/api-docs/3.2/#operations-Enum_Body-Enum_Body) |
| [List Colors](actions/list-colors.md) | `GET /:apiKey/:controlSum/decode/value-list/enum/enum_color.:format` | [docs](https://vincario.com/api-docs/3.2/#operations-Enum_Color-Enum_Color) |
| [List Drive Types](actions/list-drive-types.md) | `GET /:apiKey/:controlSum/decode/value-list/enum/enum_drive.:format` | [docs](https://vincario.com/api-docs/3.2/#operations-Enum_Drive-Enum_Drive) |
| [List Fuel Types](actions/list-fuel-types.md) | `GET /:apiKey/:controlSum/decode/value-list/enum/enum_fuel.:format` | [docs](https://vincario.com/api-docs/3.2/#operations-Enum_Fuel-Enum_Fuel) |
| [List Makes](actions/list-makes.md) | `GET /:apiKey/:controlSum/decode/value-list/enum/enum_make.:format` | [docs](https://vincario.com/api-docs/3.2/#operations-Enum_Make-Enum_Make) |
| [List Models](actions/list-models.md) | `GET /:apiKey/:controlSum/decode/value-list/enum/enum_model.:format` | [docs](https://vincario.com/api-docs/3.2/#operations-Enum_Model-Enum_Model) |
| [List Product Types](actions/list-product-types.md) | `GET /:apiKey/:controlSum/decode/value-list/enum/enum_product_type.:format` | [docs](https://vincario.com/api-docs/3.2/#operations-Enum_Product_Type-Enum_Product_Type) |
| [List Transmission Types](actions/list-transmission-types.md) | `GET /:apiKey/:controlSum/decode/value-list/enum/enum_transmission.:format` | [docs](https://vincario.com/api-docs/3.2/#operations-Enum_Transmission-Enum_Transmission) |
| [List Vehicles](actions/list-vehicles.md) | `GET /:apiKey/:controlSum/decode/value-list/enum/enum_make_model.:format` | [docs](https://vincario.com/api-docs/3.2/#operations-Enum_Vehicle-Enum_Vehicle) |
| [OEM VIN Lookup](actions/oem-vin-lookup.md) | `GET /:apiKey/:controlSum/oem/:vin.:format` | [docs](https://vincario.com/api-docs/3.2/#operations-OEM_VIN_Lookup-OEM_VIN_Lookup) |
| [Stolen Check](actions/stolen-check.md) | `GET /:apiKey/:controlSum/stolen-check/:vin.:format` | [docs](https://vincario.com/api-docs/3.2/#operations-Stolen_Check-Stolen_Check) |
| [Vehicle Market Value](actions/vehicle-market-value.md) | `GET /:apiKey/:controlSum/vehicle-market-value/:vin.:format` | [docs](https://vincario.com/api-docs/3.2/#operations-Vehicle_Market_Value-Vehicle_Market_Value) |
| [VIN Decode](actions/vin-decode.md) | `GET /:apiKey/:controlSum/decode/:vin.:format` | [docs](https://vincario.com/api-docs/3.2/#operations-VIN_Decode-VIN_Decode) |
| [VIN Decode Info](actions/vin-decode-info.md) | `GET /:apiKey/:controlSum/decode/info/:vin.:format` | [docs](https://vincario.com/api-docs/3.2/#operations-VIN_Decode_Info-VIN_Decode_Info) |
