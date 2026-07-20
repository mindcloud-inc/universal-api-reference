# Validate VAT Number with Cloudmersive Data Validation

Validates a VAT number with Cloudmersive Data Validation.

## Endpoint

- **Method:** `POST`
- **Path:** `/validate/vat/lookup`
- **Base URL:** `https://api.cloudmersive.com`
- **Official documentation:** [Validate VAT Number](https://api.cloudmersive.com/docs/validate.asp)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input` | body | `object` | yes | VAT lookup request object. |
