# Add Catalog Item Identifiers with 3E Protect

## Endpoint

- **Method:** `PUT`
- **Path:** `/catalog-item/productidentifier/:source/:identifier`
- **Base URL:** `{apiBaseUrl}`
- **API:** rest
- **Official documentation:** [Add Catalog Item Identifiers](https://secure.3eonline.com/webservices/AccountServicesV2Api/swagger/Universal/swagger.json#/paths/~1api~1universal~1v1~1catalog-item~1productidentifier~1{source}~1{identifier}/put)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `source` | path | `string` | yes | Exact, case-sensitive product identifier source name agreed with 3E. |
| `identifier` | path | `string` | yes | Your product identifier value for the selected source. |
| `sourceIdentifiers[]` | body | `array<object>` | no | Product identifier pairs to add, each with a source name and identifier value. |
| `sourceIdentifiers[].source` | body | `string` | no | Exact, case-sensitive product identifier source name agreed with 3E. |
| `sourceIdentifiers[].identifier` | body | `string` | no | Your product identifier value for the selected source. |
