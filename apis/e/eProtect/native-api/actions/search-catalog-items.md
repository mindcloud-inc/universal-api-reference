# Search Catalog Items with 3E Protect

## Endpoint

- **Method:** `POST`
- **Path:** `/document-search`
- **Base URL:** `{documentSearchApiBaseUrl}`
- **API:** rest
- **Official documentation:** [Search Catalog Items](https://secure.3eonline.com/webservices/AccountServicesV2Api/swagger/UniversalDocumentSearch/swagger.json#/paths/~1api~1universaldocumentsearch~1v1~1document-search/post)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `locationName` | body | `object` | no | Filter by an existing 3E location name. Find names with List Locations. |
| `locationName.value` | body | `string` | no | Location name returned by List Locations. |
| `locationName.compareOption` | body | `list<string>` | no | Choose Equals for an exact location name or another documented comparison. Accepted values: `BeginsWith`, `Between`, `Contains`, `Equals`, `GreaterThan`, `LessThan`. |
| `productName` | body | `object` | no | — |
| `productName.value` | body | `string` | no | — |
| `productName.compareOption` | body | `list<string>` | no | Accepted values: `BeginsWith`, `Between`, `Contains`, `Equals`, `GreaterThan`, `LessThan`. |
| `manufacturerName` | body | `object` | no | — |
| `manufacturerName.value` | body | `string` | no | — |
| `manufacturerName.compareOption` | body | `list<string>` | no | Accepted values: `BeginsWith`, `Between`, `Contains`, `Equals`, `GreaterThan`, `LessThan`. |
| `manufacturerPartNumber` | body | `object` | no | — |
| `manufacturerPartNumber.value` | body | `string` | no | — |
| `manufacturerPartNumber.compareOption` | body | `list<string>` | no | Accepted values: `BeginsWith`, `Between`, `Contains`, `Equals`, `GreaterThan`, `LessThan`. |
| `casNumber` | body | `object` | no | CAS means Chemical Abstracts Service; its registry number identifies a chemical substance. |
| `casNumber.value` | body | `string` | no | — |
| `casNumber.compareOption` | body | `list<string>` | no | Accepted values: `BeginsWith`, `Between`, `Contains`, `Equals`, `GreaterThan`, `LessThan`. |
| `sdsCountry` | body | `object` | no | — |
| `sdsCountry.value` | body | `string` | no | — |
| `sdsCountry.compareOption` | body | `list<string>` | no | Accepted values: `BeginsWith`, `Between`, `Contains`, `Equals`, `GreaterThan`, `LessThan`. |
| `uniqueIdentifiers[]` | body | `array<object>` | no | Filter using customer product identifier source and value pairs. Sources are available from List Product Identifier Sources. |
| `uniqueIdentifiers[].source` | body | `string` | no | — |
| `uniqueIdentifiers[].value` | body | `string` | no | — |
| `uniqueIdentifiers[].compareOption` | body | `list<string>` | no | Accepted values: `BeginsWith`, `Between`, `Contains`, `Equals`, `GreaterThan`, `LessThan`. |
| `customValues[]` | body | `array<object>` | no | Filter customer-defined fields by name, value and comparison. Field names are available from List Custom Value Names. |
| `customValues[].name` | body | `string` | no | — |
| `customValues[].value` | body | `string` | no | — |
| `customValues[].compareOption` | body | `list<string>` | no | Accepted values: `BeginsWith`, `Between`, `Contains`, `Equals`, `GreaterThan`, `LessThan`. |
| `lastAlteredDate` | body | `object` | no | — |
| `lastAlteredDate.valueMin` | body | `date` | no | — |
| `lastAlteredDate.valueMax` | body | `date` | no | — |
| `lastAlteredDate.compareOption` | body | `list<string>` | no | Accepted values: `BeginsWith`, `Between`, `Contains`, `Equals`, `GreaterThan`, `LessThan`. |
