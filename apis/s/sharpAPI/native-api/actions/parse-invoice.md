# Parse Invoice with SharpAPI

Creates an invoice parsing job in SharpAPI.

## Endpoint

- **Method:** `POST`
- **Path:** `/finance/parse_invoice`
- **Base URL:** `https://sharpapi.com/api/v1`
- **Official documentation:** [Parse Invoice](https://sharpapi.com/en/catalog/ai/accounting-finance/invoice-parser)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | Invoice document file to parse. |
| `language` | body | `string` | no | Language used for invoice parsing. |
