# Enable DNSSEC with BunnyCDN

Enables DNSSEC for a BunnyCDN DNS zone.

## Endpoint

- **Method:** `POST`
- **Path:** `/dnszone/:id/dnssec`
- **Base URL:** `https://api.bunny.net`
- **Official documentation:** [Enable DNSSEC](https://docs.bunny.net/reference/bunnynet-api-overview)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Bunny DNS zone ID. |
