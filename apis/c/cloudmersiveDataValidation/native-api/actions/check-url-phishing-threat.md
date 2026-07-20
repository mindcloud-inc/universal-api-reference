# Check URL Phishing Threat with Cloudmersive Data Validation

Checks a URL for phishing threats with Cloudmersive Data Validation.

## Endpoint

- **Method:** `POST`
- **Path:** `/validate/domain/url/phishing-threat-check`
- **Base URL:** `https://api.cloudmersive.com`
- **Official documentation:** [Check URL Phishing Threat](https://api.cloudmersive.com/docs/validate.asp)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `request` | body | `object` | yes | URL threat-check request object containing the URL to check. |
