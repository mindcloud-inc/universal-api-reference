# Search Sessions with SalesViewer

Finds sessions in SalesViewer by query parameters.

## Endpoint

- **Method:** `GET`
- **Path:** `/sessions.json`
- **Base URL:** `https://api.salesviewer.com/`
- **Official documentation:** [Search Sessions](https://salesviewer.github.io/salesviewer-api/definition)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | query | `string` | no | Starting datetime for the session query. |
| `includeCompany` | query | `boolean` | no | Include company details in each session. |
| `includeCompanySector` | query | `boolean` | no | Include company sector when company data is requested. |
| `includeHidden` | query | `boolean` | no | Include frontend-hidden companies. |
| `includeVisits` | query | `boolean` | no | Include visit details in each session. |
| `locale` | query | `string` | no | Locale used for localized output fields. |
| `page` | query | `number` | no | 1-based result page number. |
| `pageSize` | query | `number` | no | Number of entries per page. |
| `query` | query | `string` | no | SVQL query string used to filter sessions. |
| `timezone` | query | `string` | no | Timezone used for input and output datetimes. |
| `to` | query | `string` | no | Ending datetime for the session query. |
