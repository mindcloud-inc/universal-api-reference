# Validate Postal Code with Cloudmersive Data Validation

Validates a postal code with Cloudmersive Data Validation.

## Endpoint

- **Method:** `POST`
- **Path:** `/validate/address/postal-code`
- **Base URL:** `https://api.cloudmersive.com`
- **Official documentation:** [Validate Postal Code](https://api.cloudmersive.com/docs/validate.asp)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input` | body | `object` | yes | Postal code validation request object containing postal code and country details. |
