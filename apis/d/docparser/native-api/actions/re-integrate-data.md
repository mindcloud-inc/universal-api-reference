# Re-Integrate Data with Docparser

Schedules Docparser documents for re-integration.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/document/reintegrate/:PARSER_ID`
- **Base URL:** `https://api.docparser.com`
- **Official documentation:** [Re-Integrate Data](https://docparser.com/api/#re-integrate-data)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `PARSER_ID` | path | `string` | yes |
| `document_ids[]` | body | `array<string>` | yes |
