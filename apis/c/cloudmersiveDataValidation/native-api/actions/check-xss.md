# Check XSS with Cloudmersive Data Validation

Checks text input for XSS with Cloudmersive Data Validation.

## Endpoint

- **Method:** `POST`
- **Path:** `/validate/text-input/check/xss`
- **Base URL:** `https://api.cloudmersive.com`
- **Official documentation:** [Check XSS](https://api.cloudmersive.com/docs/validate.asp)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `value` | body | `string` | yes | Text input to check for cross-site scripting attacks. |
