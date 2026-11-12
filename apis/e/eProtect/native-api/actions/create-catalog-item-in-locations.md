# Create Catalog Item in Locations with 3E Protect

## Endpoint

- **Method:** `POST`
- **Path:** `/catalog-item-inventory`
- **Base URL:** `{apiBaseUrl}`
- **API:** rest
- **Official documentation:** [Create Catalog Item in Locations](https://secure.3eonline.com/webservices/AccountServicesV2Api/swagger/Universal/swagger.json#/paths/~1api~1universal~1v1~1catalog-item-inventory/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `manufacturerName` | body | `string` | yes | — |
| `materialName` | body | `string` | yes | — |
| `productNumber` | body | `string` | no | — |
| `locationNames[]` | body | `array<string>` | yes | Existing 3E location names. Retrieve them with List Locations. |
| `customValues[]` | body | `array<object>` | no | Customer-defined product fields, each supplied as a name and value. |
| `customValues[].name` | body | `string` | no | — |
| `customValues[].value` | body | `string` | no | — |
| `source` | body | `string` | yes | Exact, case-sensitive product identifier source name agreed with 3E. |
| `identifier` | body | `string` | yes | Your product identifier value for the selected source. |
