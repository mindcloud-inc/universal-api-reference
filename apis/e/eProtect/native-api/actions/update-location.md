# Update Location with 3E Protect

## Endpoint

- **Method:** `PUT`
- **Path:** `/location`
- **Base URL:** `{apiBaseUrl}`
- **API:** rest
- **Official documentation:** [Update Location](https://secure.3eonline.com/webservices/AccountServicesV2Api/swagger/Universal/swagger.json#/paths/~1api~1universal~1v1~1location/put)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `currentName` | body | `string` | yes |
| `name` | body | `string` | yes |
| `countryCode` | body | `string` | yes |
| `keyWords[]` | body | `array<string>` | no |
