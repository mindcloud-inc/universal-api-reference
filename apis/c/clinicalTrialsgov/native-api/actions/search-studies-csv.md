# Search Studies CSV with ClinicalTrials.gov

## Endpoint

- **Method:** `GET`
- **Path:** `/studies`
- **Base URL:** `https://clinicaltrials.gov/api/v2`
- **Official documentation:** [Search Studies CSV](https://clinicaltrials.gov/data-api/about-api/csv-download)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `aggFilters` | query | `string` | no | Apply aggregate filters using the API's filter syntax. |
| `countTotal` | query | `boolean` | no | Include the total number of matching studies. |
| `fields` | query | `string` | no | Return only selected fields. |
| `filter.geo` | query | `string` | no | Filter results by geographic bounding or distance query. |
| `filter.overallStatus` | query | `string` | no | Filter results by study status. |
| `pageSize` | query | `number` | no | Number of studies to return. |
| `pageToken` | query | `string` | no | Cursor token for the next page. |
| `query.cond` | query | `string` | no | Search by condition or disease terms. |
| `query.id` | query | `string` | no | Search by NCT ID or other study identifiers. |
| `query.intr` | query | `string` | no | Search by intervention or treatment terms. |
| `query.lead` | query | `string` | no | Search by lead sponsor terms. |
| `query.locn` | query | `string` | no | Search by location terms. |
| `query.outc` | query | `string` | no | Search by outcome measure terms. |
| `query.patient` | query | `string` | no | Search by patient-facing terms. |
| `query.spons` | query | `string` | no | Search by sponsor or collaborator terms. |
| `query.term` | query | `string` | no | Search by keyword terms. |
| `query.titles` | query | `string` | no | Search by brief title, official title, or acronym. |
| `sort` | query | `string` | no | Sort the result set. |
