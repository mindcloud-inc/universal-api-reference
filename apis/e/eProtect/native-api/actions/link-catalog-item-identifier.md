# Link Catalog Item Identifier with 3E Protect

## Endpoint

- **Method:** `PUT`
- **Path:** `/link-catalog-item/:eeeProductUid/:source/:identifier`
- **Base URL:** `{apiBaseUrl}`
- **API:** rest
- **Official documentation:** [Link Catalog Item Identifier](https://secure.3eonline.com/webservices/AccountServicesV2Api/swagger/Universal/swagger.json#/paths/~1api~1universal~1v1~1link-catalog-item~1{eeeProductUid}~1{source}~1{identifier}/put)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `eeeProductUid` | path | `string` | yes | 3E product UID (unique record identifier) returned by List Unlinked Catalog Items. |
| `source` | path | `string` | yes | Exact, case-sensitive product identifier source name agreed with 3E. |
| `identifier` | path | `string` | yes | Your product identifier value for the selected source. |
