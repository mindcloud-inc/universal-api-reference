# Check IP Threat with Cloudmersive Security

Checks an IP address for threats in Cloudmersive Security.

## Endpoint

- **Method:** `POST`
- **Path:** `/security/threat-detection/network/ip/is-threat`
- **Base URL:** `https://api.cloudmersive.com`
- **Official documentation:** [Check IP Threat](https://api.cloudmersive.com/docs/security.asp)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ipAddress` | body | `string` | yes | IP address to check, for example 55.55.55.55. |
