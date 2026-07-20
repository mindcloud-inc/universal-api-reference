# Re-Parse Data with Docparser

Schedules Docparser documents for re-parsing.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/document/reparse/:PARSER_ID`
- **Base URL:** `https://api.docparser.com`
- **Official documentation:** [Re-Parse Data](https://docparser.com/api/#re-parse-data)

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
