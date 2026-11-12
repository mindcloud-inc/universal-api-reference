# Get Catalog Item by Language and Country with 3E Protect

## Endpoint

- **Method:** `GET`
- **Path:** `/catalog-item/:source/:identifier/:locale/:country`
- **Base URL:** `{apiBaseUrl}`
- **API:** rest
- **Official documentation:** [Get Catalog Item by Language and Country](https://secure.3eonline.com/webservices/AccountServicesV2Api/swagger/Universal/swagger.json#/paths/~1api~1universal~1v1~1catalog-item~1{source}~1{identifier}~1{locale}~1{country}/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `source` | path | `string` | yes | Exact, case-sensitive product identifier source name agreed with 3E. |
| `identifier` | path | `string` | yes | Your product identifier value for the selected source. |
| `country` | path | `string` | yes | Three-letter country code, such as USA. Use a country configured in List SDS Requirements. |
| `locale` | path | `string` | yes | Two-letter language code, such as en. Use a language configured in List SDS Requirements. |
