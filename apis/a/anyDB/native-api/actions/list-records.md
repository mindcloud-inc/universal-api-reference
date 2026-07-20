# List Records with AnyDB

Retrieves records from AnyDB with optional filters and pagination.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/integrations/ext/list`
- **Base URL:** `https://app.anydb.com`
- **Official documentation:** [List Records](https://www.anydb.com/openapi/spec.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `teamid` | query | `string` | yes | The AnyDB team ID. |
| `adbid` | query | `string` | yes | The AnyDB database ID. |
| `groupby` | query | `string` | no | Optional AnyDB group-by field. |
| `templateid` | query | `string` | no | Optional template ID to filter by. |
| `templatename` | query | `string` | no | Optional template name to filter by. |
| `parentid` | query | `string` | no | Optional parent record ID to scope the listing. |
| `pagesize` | query | `number` | no | Optional page size for the listing. |
| `lastmarker` | query | `string` | no | Optional pagination marker from a previous response. |
| `sort` | query | `string` | no | Optional JSON string describing AnyDB sort instructions. |
| `filter` | query | `string` | no | Optional JSON string describing AnyDB filter rules. |
| `previewcells` | query | `string` | no | Optional JSON string describing which cells to preview. |
