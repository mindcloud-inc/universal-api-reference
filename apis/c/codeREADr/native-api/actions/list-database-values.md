# List Database Values with CodeREADr

Retrieves values from a validation database in CodeREADr.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/`
- **Base URL:** `https://api.codereadr.com`
- **Official documentation:** [List Database Values](https://secure.codereadr.com/apidocs/Databases.md#showvalues)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `database_id` | body | `string` | yes | Database to search. |
| `value` | body | `string` | no | Exact barcode value match. |
| `valuelike` | body | `string` | no | Partial barcode value match. |
| `response` | body | `string` | no | Exact response text match. |
| `responselike` | body | `string` | no | Partial response text match. |
| `validity` | body | `string` | no | Filter by valid (1) or invalid (0). |
| `limit` | body | `string` | no | Maximum number of results to return. |
| `offset` | body | `string` | no | Result offset when limit is provided. |
