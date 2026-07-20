# Search Opportunities with Grants.gov

Finds grant opportunities in Grants.gov by public search filters.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/api/search2`
- **Base URL:** `https://api.grants.gov`
- **Official documentation:** [Search Opportunities](https://grants.gov/api/common/search2)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `keyword` | body | `string` | no | Keyword search over public grant opportunity titles and details. |
| `oppNum` | body | `string` | no | Funding Opportunity Number to search for. |
| `cfda` | body | `string` | no | CFDA or Assistance Listing Number. This key is runtime-verified even though the docs sample still shows aln. |
| `agencies` | body | `string` | no | Agency or sub-agency code filter such as HHS or HHS-NIH11. |
| `eligibilities` | body | `string` | no | Eligibility code filter such as 01 for county governments. |
| `fundingCategories` | body | `string` | no | Funding activity category code such as HL for Health. |
| `oppStatuses` | body | `list` | no | One or more opportunity statuses to include. Accepted values: `archived`, `closed`, `forecasted`, `posted`. Send multiple values as a string separated by `\|`. |
| `rows` | body | `number` | no | Maximum number of opportunities to return. |
| `fundingInstruments` | body | `string` | no | Funding instrument code such as G for Grant or CA for Cooperative Agreement. |
| `startRecordNum` | body | `number` | no | Zero-based record offset for paged search results. |
