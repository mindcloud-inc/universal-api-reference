# Check IP Bot Status with Cloudmersive Security

Checks an IP address for bot threats in Cloudmersive Security.

## Endpoint

- **Method:** `POST`
- **Path:** `/security/threat-detection/network/ip/is-bot`
- **Base URL:** `https://api.cloudmersive.com`
- **Official documentation:** [Check IP Bot Status](https://api.cloudmersive.com/docs/security.asp)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ipAddress` | body | `string` | yes | IP address to check, for example 55.55.55.55. |
