# Set Catalog Item Custom Values with 3E Protect

## Endpoint

- **Method:** `PUT`
- **Path:** `/catalog-item/customvalue/:source/:identifier`
- **Base URL:** `{apiBaseUrl}`
- **API:** rest
- **Official documentation:** [Set Catalog Item Custom Values](https://secure.3eonline.com/webservices/AccountServicesV2Api/swagger/Universal/swagger.json#/paths/~1api~1universal~1v1~1catalog-item~1customvalue~1{source}~1{identifier}/put)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `source` | path | `string` | yes | Exact, case-sensitive product identifier source name agreed with 3E. |
| `identifier` | path | `string` | yes | Your product identifier value for the selected source. |
| `customValues[]` | body | `array<object>` | yes | Customer-defined product fields, each supplied as a name and value. |
| `customValues[].name` | body | `string` | no | — |
| `customValues[].value` | body | `string` | no | — |
