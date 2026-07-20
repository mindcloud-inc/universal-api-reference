# Check URL Safety Threat with Cloudmersive Data Validation

Checks a URL for safety threats with Cloudmersive Data Validation.

## Endpoint

- **Method:** `POST`
- **Path:** `/validate/domain/url/safety-threat-check`
- **Base URL:** `https://api.cloudmersive.com`
- **Official documentation:** [Check URL Safety Threat](https://api.cloudmersive.com/docs/validate.asp)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `request` | body | `object` | yes | URL safety threat-check request object containing the URL to check. |
