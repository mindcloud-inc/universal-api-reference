# Validate CFDI from PDF with ValidaCFDI

Validates a CFDI from a PDF in ValidaCFDI.

## Endpoint

- **Method:** `POST`
- **Path:** `/validate/pdf`
- **Base URL:** `https://api.valida-cfdi.com.mx/v1`
- **Official documentation:** [Validate CFDI from PDF](https://valida-cfdi.com.mx/docs/api)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | PDF invoice file to validate and extract. |
