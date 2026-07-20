# Validate URL Syntax with Cloudmersive Data Validation

Validates URL syntax with Cloudmersive Data Validation.

## Endpoint

- **Method:** `POST`
- **Path:** `/validate/domain/url/syntax-only`
- **Base URL:** `https://api.cloudmersive.com`
- **Official documentation:** [Validate URL Syntax](https://api.cloudmersive.com/docs/validate.asp)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `request` | body | `object` | yes | ValidateUrlRequestSyntaxOnly object, for example {"URL":"https://cloudmersive.com"}. |
