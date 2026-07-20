# Search Studies with ClinicalTrials.gov

## Endpoint

- **Method:** `GET`
- **Path:** `/studies`
- **Base URL:** `https://clinicaltrials.gov/api/v2`
- **Official documentation:** [Search Studies](https://clinicaltrials.gov/data-api/api)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `aggFilters` | query | `string` | no | Apply aggregate filters using the API's filter syntax. |
| `fields` | query | `string` | no | Return only selected fields. |
| `filter.geo` | query | `string` | no | Filter results by geographic bounding or distance query. |
| `filter.overallStatus` | query | `string` | no | Filter results by study status. |
| `pageToken` | query | `string` | no | Cursor token for the next page. |
| `query.cond` | query | `string` | no | Search within condition fields. |
| `query.id` | query | `string` | no | Search by NCT ID or other identifiers. |
| `query.intr` | query | `string` | no | Search within intervention fields. |
| `query.lead` | query | `string` | no | Search within lead sponsor fields. |
| `query.locn` | query | `string` | no | Search by study location text. |
| `query.outc` | query | `string` | no | Search within outcome fields. |
| `query.patient` | query | `string` | no | Search patient-facing terms. |
| `query.spons` | query | `string` | no | Search within sponsor fields. |
| `query.term` | query | `string` | no | Search across the default BasicSearch area. |
| `query.titles` | query | `string` | no | Search within study title fields. |
| `sort` | query | `string` | no | Sort the result set. |
| `countTotal` | query | `boolean` | no | Include the total number of matching studies. |
| `pageSize` | query | `number` | no | Number of studies to return. |
| `format` | query | `string` | no | Response format. Accepted values: `0`, `1`. |
