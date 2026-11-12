# Create Location with 3E Protect

## Endpoint

- **Method:** `POST`
- **Path:** `/location`
- **Base URL:** `{apiBaseUrl}`
- **API:** rest
- **Official documentation:** [Create Location](https://secure.3eonline.com/webservices/AccountServicesV2Api/swagger/Universal/swagger.json#/paths/~1api~1universal~1v1~1location/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | — |
| `parentName` | body | `string` | no | Existing parent location name, using the exact capitalization returned by List Locations. |
| `countryCode` | body | `string` | yes | — |
| `keyWords[]` | body | `array<string>` | no | — |
| `obtainment` | body | `object` | yes | SDS obtainment (sourcing) language and country for this location. |
| `obtainment.locale` | body | `string` | no | Two-letter language code, such as en. Use a language configured in List SDS Requirements. |
| `obtainment.country` | body | `string` | no | Three-letter country code, such as USA. Use a country configured in List SDS Requirements. |
