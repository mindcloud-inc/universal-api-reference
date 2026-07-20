# Get IP Intelligence with Cloudmersive Data Validation

Retrieves IP intelligence from Cloudmersive Data Validation.

## Endpoint

- **Method:** `POST`
- **Path:** `/validate/ip/intelligence`
- **Base URL:** `https://api.cloudmersive.com`
- **Official documentation:** [Get IP Intelligence](https://api.cloudmersive.com/docs/validate.asp)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `value` | body | `string` | yes | IP address to inspect. |
