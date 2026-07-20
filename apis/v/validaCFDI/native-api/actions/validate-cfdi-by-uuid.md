# Validate CFDI by UUID with ValidaCFDI

Validates a CFDI by UUID in ValidaCFDI.

## Endpoint

- **Method:** `POST`
- **Path:** `/validate`
- **Base URL:** `https://api.valida-cfdi.com.mx/v1`
- **Official documentation:** [Validate CFDI by UUID](https://valida-cfdi.com.mx/docs/api)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uuid` | body | `string` | yes | CFDI UUID to validate. |
| `rfc_emisor` | body | `string` | yes | RFC of the CFDI issuer. |
| `rfc_receptor` | body | `string` | yes | RFC of the CFDI receiver. |
| `total` | body | `number` | yes | Total invoice amount for validation. |
