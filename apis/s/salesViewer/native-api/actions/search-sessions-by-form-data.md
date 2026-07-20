# Search Sessions by Form Data with SalesViewer

Finds sessions in SalesViewer by form data.

## Endpoint

- **Method:** `POST`
- **Path:** `/sessions.json`
- **Base URL:** `https://api.salesviewer.com/`
- **Official documentation:** [Search Sessions by Form Data](https://salesviewer.github.io/salesviewer-api/definition)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | body | `string` | no | Starting datetime for the session query. |
| `includeCompany` | body | `boolean` | no | Include company details in each session. |
| `includeCompanySector` | body | `boolean` | no | Include company sector when company data is requested. |
| `includeHidden` | body | `boolean` | no | Include frontend-hidden companies. |
| `includeVisits` | body | `boolean` | no | Include visit details in each session. |
| `locale` | body | `string` | no | Locale used for localized output fields. |
| `page` | body | `number` | no | 1-based result page number. |
| `pageSize` | body | `number` | no | Number of entries per page. |
| `query` | body | `string` | no | SVQL query string used to filter sessions. |
| `timezone` | body | `string` | no | Timezone used for input and output datetimes. |
| `to` | body | `string` | no | Ending datetime for the session query. |
