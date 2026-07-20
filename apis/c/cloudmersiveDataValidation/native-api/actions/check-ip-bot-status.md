# Check IP Bot Status with Cloudmersive Data Validation

Checks whether an IP is a bot client.

## Endpoint

- **Method:** `POST`
- **Path:** `/validate/ip/is-bot`
- **Base URL:** `https://api.cloudmersive.com`
- **Official documentation:** [Check IP Bot Status](https://api.cloudmersive.com/docs/validate.asp)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `value` | body | `string` | yes | IP address to check for bot status. |
