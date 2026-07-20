# Check SQL Injection with Cloudmersive Data Validation

Checks text input for SQL injection with Cloudmersive Data Validation.

## Endpoint

- **Method:** `POST`
- **Path:** `/validate/text-input/check/sql-injection`
- **Base URL:** `https://api.cloudmersive.com`
- **Official documentation:** [Check SQL Injection](https://api.cloudmersive.com/docs/validate.asp)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `value` | body | `string` | yes | Text input to check for SQL injection attacks. |
