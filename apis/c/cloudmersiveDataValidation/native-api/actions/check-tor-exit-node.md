# Check Tor Exit Node with Cloudmersive Data Validation

Checks whether an IP is a Tor node.

## Endpoint

- **Method:** `POST`
- **Path:** `/validate/ip/is-tor-node`
- **Base URL:** `https://api.cloudmersive.com`
- **Official documentation:** [Check Tor Exit Node](https://api.cloudmersive.com/docs/validate.asp)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `value` | body | `string` | yes | IP address to check for Tor node status. |
