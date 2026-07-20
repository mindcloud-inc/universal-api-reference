# Get IP Lookup with Ipregistry

## Endpoint

- **Method:** `GET`
- **Path:** `/:ipAddress`
- **Base URL:** `https://api.ipregistry.co`
- **Official documentation:** [Get IP Lookup](https://ipregistry.co/docs/endpoints#single-ip)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ipAddress` | path | `string` | yes | IPv4 or IPv6 address to look up. |
| `fields` | query | `string` | no | Optional response filter. Example: `location.country.name,security.is_tor`. |
| `hostname` | query | `boolean` | no | Set to true to include a fresh reverse DNS hostname lookup. |
