# Get Batch IP Lookup with Ipregistry

## Endpoint

- **Method:** `GET`
- **Path:** `/:ipAddresses`
- **Base URL:** `https://api.ipregistry.co`
- **Official documentation:** [Get Batch IP Lookup](https://ipregistry.co/docs/endpoints#batch-ip)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ipAddresses` | path | `string` | yes | Comma-separated list of up to 1024 IPv4 or IPv6 addresses. |
| `fields` | query | `string` | no | Optional response filter applied to each result item. |
