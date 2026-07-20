# Check URL SSRF Threat with Cloudmersive Data Validation

Checks a URL for SSRF threats with Cloudmersive Data Validation.

## Endpoint

- **Method:** `POST`
- **Path:** `/validate/domain/url/ssrf-threat-check`
- **Base URL:** `https://api.cloudmersive.com`
- **Official documentation:** [Check URL SSRF Threat](https://api.cloudmersive.com/docs/validate.asp)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `request` | body | `object` | yes | URL SSRF threat-check request object containing the URL to check. |
