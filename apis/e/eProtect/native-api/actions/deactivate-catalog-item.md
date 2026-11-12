# Deactivate Catalog Item with 3E Protect

## Endpoint

- **Method:** `DELETE`
- **Path:** `/catalog-item/:source/:identifier`
- **Base URL:** `{apiBaseUrl}`
- **API:** rest
- **Official documentation:** [Deactivate Catalog Item](https://secure.3eonline.com/webservices/AccountServicesV2Api/swagger/Universal/swagger.json#/paths/~1api~1universal~1v1~1catalog-item~1{source}~1{identifier}/delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `source` | path | `string` | yes | Exact, case-sensitive product identifier source name agreed with 3E. |
| `identifier` | path | `string` | yes | Your product identifier value for the selected source. |
