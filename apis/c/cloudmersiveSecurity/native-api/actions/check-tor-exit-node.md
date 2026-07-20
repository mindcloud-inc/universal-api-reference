# Check Tor Exit Node with Cloudmersive Security

Checks whether an IP is a Tor node in Cloudmersive Security.

## Endpoint

- **Method:** `POST`
- **Path:** `/security/threat-detection/network/ip/is-tor-node`
- **Base URL:** `https://api.cloudmersive.com`
- **Official documentation:** [Check Tor Exit Node](https://api.cloudmersive.com/docs/security.asp)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ipAddress` | body | `string` | yes | IP address to check, for example 55.55.55.55. |
