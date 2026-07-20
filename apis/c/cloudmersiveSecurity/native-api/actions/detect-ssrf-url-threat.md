# Detect SSRF URL Threat with Cloudmersive Security

Checks a URL for SSRF threats in Cloudmersive Security.

## Endpoint

- **Method:** `POST`
- **Path:** `/security/threat-detection/network/url/ssrf/detect`
- **Base URL:** `https://api.cloudmersive.com`
- **Official documentation:** [Detect SSRF URL Threat](https://api.cloudmersive.com/docs/security.asp)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `URL` | body | `string` | yes | URL to check for SSRF threat risk. |
| `BlockedDomains[]` | body | `array<string>` | no | Optional domains to block. Each entry blocks that domain and its subdomains. Send multiple values as a array. |
