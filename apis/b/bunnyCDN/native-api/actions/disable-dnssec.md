# Disable DNSSEC with BunnyCDN

Disables DNSSEC for a BunnyCDN DNS zone.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/dnszone/:id/dnssec`
- **Base URL:** `https://api.bunny.net`
- **Official documentation:** [Disable DNSSEC](https://docs.bunny.net/reference/bunnynet-api-overview)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Bunny DNS zone ID. |
