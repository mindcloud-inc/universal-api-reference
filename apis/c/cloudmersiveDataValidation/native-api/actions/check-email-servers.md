# Check Email Servers with Cloudmersive Data Validation

Checks email servers for an address with Cloudmersive Data Validation.

## Endpoint

- **Method:** `POST`
- **Path:** `/validate/email/address/servers`
- **Base URL:** `https://api.cloudmersive.com`
- **Official documentation:** [Check Email Servers](https://api.cloudmersive.com/docs/validate.asp)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Email address to validate against mail servers. |
