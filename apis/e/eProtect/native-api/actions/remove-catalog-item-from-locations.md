# Remove Catalog Item from Locations with 3E Protect

## Endpoint

- **Method:** `DELETE`
- **Path:** `/catalog-item-inventory`
- **Base URL:** `{apiBaseUrl}`
- **API:** rest
- **Official documentation:** [Remove Catalog Item from Locations](https://secure.3eonline.com/webservices/AccountServicesV2Api/swagger/Universal/swagger.json#/paths/~1api~1universal~1v1~1catalog-item-inventory/delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `source` | body | `string` | yes | Exact, case-sensitive product identifier source name agreed with 3E. |
| `identifier` | body | `string` | yes | Your product identifier value for the selected source. |
| `locationNames[]` | body | `array<string>` | yes | Existing 3E location names. Retrieve them with List Locations. |
