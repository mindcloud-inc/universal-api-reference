# Create Catalog Item with SDS Attachment with 3E Protect

## Endpoint

- **Method:** `POST`
- **Path:** `/catalog-item-attachment`
- **Base URL:** `{apiBaseUrl}`
- **API:** rest
- **Official documentation:** [Create Catalog Item with SDS Attachment](https://secure.3eonline.com/webservices/AccountServicesV2Api/swagger/Universal/swagger.json#/paths/~1api~1universal~1v1~1catalog-item-attachment/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileBytes` | body | `string` | yes | PDF contents encoded as Base64, a text representation of file bytes. |
| `fileName` | body | `string` | yes | PDF file name, including the .pdf extension. |
| `manufacturerName` | body | `string` | yes | — |
| `materialName` | body | `string` | yes | — |
| `obtainmentTypes[]` | body | `array<object>` | yes | SDS obtainment (sourcing) targets, each defined by a language and country. |
| `obtainmentTypes[].locale` | body | `string` | no | Two-letter language code, such as en. Use a language configured in List SDS Requirements. |
| `obtainmentTypes[].country` | body | `string` | no | Three-letter country code, such as USA. Use a country configured in List SDS Requirements. |
| `productNumber` | body | `string` | no | — |
| `source` | body | `string` | yes | Exact, case-sensitive product identifier source name agreed with 3E. |
| `identifier` | body | `string` | yes | Your product identifier value for the selected source. |
| `customValues[]` | body | `array<object>` | no | Customer-defined product fields, each supplied as a name and value. |
| `customValues[].name` | body | `string` | no | — |
| `customValues[].value` | body | `string` | no | — |
