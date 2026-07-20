# Validate Domain Name with Cloudmersive Data Validation

Validates a domain name with Cloudmersive Data Validation.

## Endpoint

- **Method:** `POST`
- **Path:** `/validate/domain/check`
- **Base URL:** `https://api.cloudmersive.com`
- **Official documentation:** [Validate Domain Name](https://api.cloudmersive.com/docs/validate.asp)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | body | `string` | yes | Domain name to validate. |
