# Search Awards with National Science Foundation

Finds awards in National Science Foundation by search criteria.

## Endpoint

- **Method:** `GET`
- **Path:** `/awards.json`
- **Base URL:** `https://api.nsf.gov/services/v1`
- **Official documentation:** [Search Awards](https://resources.research.gov/common/webapi/awardapisearch-v1.htm)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `keyword` | query | `string` | no | Free-text search across all available award data. Boolean operators AND, OR, and NOT are supported by the NSF API. |
| `ActiveAwards` | query | `boolean` | no | Set to true to include active awards. |
| `ExpiredAwards` | query | `boolean` | no | Set to true to include expired awards. |
| `awardeeName` | query | `string` | no | Name of the entity receiving the award. |
| `pdPIName` | query | `string` | no | Project Director or Principal Investigator name. |
| `poName` | query | `string` | no | NSF program officer name. |
| `fundProgramName` | query | `string` | no | NSF fund program name. |
| `cfdaNumber` | query | `string` | no | Catalog of Federal Domestic Assistance number, such as 47.084. |
| `awardeeStateCode` | query | `string` | no | Awardee state abbreviation, such as VA. |
| `awardeeCountryCode` | query | `string` | no | Awardee country code, such as US. |
| `perfLocation` | query | `string` | no | Performance location name. |
| `perfStateCode` | query | `string` | no | Performance state abbreviation, such as VA. |
| `ProgEleCode` | query | `string` | no | NSF program element code, a six-digit PEC such as 999300. |
| `ProgRefCode` | query | `string` | no | NSF program reference code. |
| `org_code_dir` | query | `string` | no | Directorate organization code, an eight-digit code such as 15000000. |
| `org_code_div` | query | `string` | no | Division organization code, an eight-digit code such as 15030000. |
| `dateStart` | query | `string` | no | Start date for award date search. NSF expects mm/dd/yyyy, such as 12/31/2012. |
| `dateEnd` | query | `string` | no | End date for award date search. NSF expects mm/dd/yyyy, such as 12/31/2012. |
| `startDateStart` | query | `string` | no | Start date for award start date search. NSF expects mm/dd/yyyy. |
| `startDateEnd` | query | `string` | no | End date for award start date search. NSF expects mm/dd/yyyy. |
| `expDateStart` | query | `string` | no | Start date for award expiration date search. NSF expects mm/dd/yyyy. |
| `expDateEnd` | query | `string` | no | End date for award expiration date search. NSF expects mm/dd/yyyy. |
| `estimatedTotalAmtFrom` | query | `number` | no | Return awards greater than this estimated total amount. |
| `estimatedTotalAmtTo` | query | `number` | no | Return awards less than this estimated total amount. |
| `fundsObligatedAmtFrom` | query | `number` | no | Return awards greater than this obligated amount. |
| `fundsObligatedAmtTo` | query | `number` | no | Return awards less than this obligated amount. |
| `transType` | query | `string` | no | Award transaction type, such as Standard Grant, Continuing Grant, Cooperative Agreement, or Fellowship Award. |
| `ueiNumber` | query | `string` | no | Unique Entity Identifier, such as F2VSMAKDH8Z7. |
