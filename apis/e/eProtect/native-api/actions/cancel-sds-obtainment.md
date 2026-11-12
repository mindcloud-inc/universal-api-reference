# Cancel SDS Obtainment with 3E Protect

## Endpoint

- **Method:** `PUT`
- **Path:** `/customer-action-cancel-obtainment`
- **Base URL:** `{apiBaseUrl}`
- **API:** rest
- **Official documentation:** [Cancel SDS Obtainment](https://secure.3eonline.com/webservices/AccountServicesV2Api/swagger/Universal/swagger.json#/paths/~1api~1universal~1v1~1customer-action-cancel-obtainment/put)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `source` | body | `string` | yes | Exact, case-sensitive product identifier source name agreed with 3E. |
| `uniqueId` | body | `string` | yes | Your catalog item identifier value for the selected source. |
| `obtainmentTypes[]` | body | `array<object>` | yes | SDS obtainment (sourcing) targets, each defined by a language and country. |
| `obtainmentTypes[].locale` | body | `string` | no | Two-letter language code, such as en. Use a language configured in List SDS Requirements. |
| `obtainmentTypes[].country` | body | `string` | no | Three-letter country code, such as USA. Use a country configured in List SDS Requirements. |
| `notes` | body | `string` | yes | — |
