# Enrich IP with People Data Labs

## Endpoint

- **Method:** `GET`
- **Path:** `/ip/enrich`
- **Base URL:** `https://api.peopledatalabs.com/v5`
- **Official documentation:** [Enrich IP](https://docs.peopledatalabs.com/docs/reference-ip-enrichment-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ip` | query | `string` | yes | IPv4 or IPv6 address to enrich. |
| `return_if_unmatched` | query | `boolean` | no | Return IP-specific metadata or location data even when no company match is found. |
| `return_ip_location` | query | `boolean` | no | Return IP-specific location info regardless of a company match. |
| `return_ip_metadata` | query | `boolean` | no | Return IP-specific metadata regardless of a company match. |
| `return_person` | query | `boolean` | no | Return person fields associated with the IP when available. |
