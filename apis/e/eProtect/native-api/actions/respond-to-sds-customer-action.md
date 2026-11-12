# Respond to SDS Customer Action with 3E Protect

## Endpoint

- **Method:** `PUT`
- **Path:** `/customer-action-notes-file`
- **Base URL:** `{apiBaseUrl}`
- **API:** rest
- **Official documentation:** [Respond to SDS Customer Action](https://secure.3eonline.com/webservices/AccountServicesV2Api/swagger/Universal/swagger.json#/paths/~1api~1universal~1v1~1customer-action-notes-file/put)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `source` | body | `string` | yes | Exact, case-sensitive product identifier source name agreed with 3E. |
| `uniqueId` | body | `string` | yes | Your catalog item identifier value for the selected source. |
| `obtainmentTypes[]` | body | `array<object>` | yes | SDS obtainment (sourcing) targets, each defined by a language and country. |
| `obtainmentTypes[].locale` | body | `string` | no | Two-letter language code, such as en. Use a language configured in List SDS Requirements. |
| `obtainmentTypes[].country` | body | `string` | no | Three-letter country code, such as USA. Use a country configured in List SDS Requirements. |
| `notes` | body | `string` | yes | — |
| `fileBytes` | body | `string` | no | PDF contents encoded as Base64, a text representation of file bytes. |
| `fileName` | body | `string` | no | PDF file name, including the .pdf extension. |
