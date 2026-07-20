# Check IP Threat with Cloudmersive Data Validation

Checks an IP address for threats with Cloudmersive Data Validation.

## Endpoint

- **Method:** `POST`
- **Path:** `/validate/ip/is-threat`
- **Base URL:** `https://api.cloudmersive.com`
- **Official documentation:** [Check IP Threat](https://api.cloudmersive.com/docs/validate.asp)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `value` | body | `string` | yes | IP address to check for threat status. |
