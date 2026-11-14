# Search Catalog Items Page with 3E Protect

## Endpoint

- **Method:** `POST`
- **Path:** `{documentSearchApiBaseUrl}/document-search`
- **Base URL:** `{apiBaseUrl}`
- **API:** rest
- **Official documentation:** [Search Catalog Items Page](https://secure.3eonline.com/webservices/AccountServicesV2Api/swagger/UniversalDocumentSearch/swagger.json#/paths/~1api~1universaldocumentsearch~1v1~1document-search/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lastAlteredDate` | body | `object` | no | — |
| `lastAlteredDate.valueMin` | body | `string` | no | Inclusive start of the fixed change-date window, formatted as an ISO 8601 timestamp. |
| `lastAlteredDate.valueMax` | body | `string` | no | End of the fixed change-date window. Keep this value unchanged while reading its subsequent pages. |
| `lastAlteredDate.compareOption` | body | `list` | no | Accepted values: `0`, `1`, `2`, `3`, `4`, `5`. |
| `pageNumber` | body | `number` | yes | The explicit 3E page number, starting at 1. |
| `pageSize` | body | `number` | yes | — |
