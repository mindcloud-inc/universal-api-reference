# Add DNS Zone with BunnyCDN

Creates a new DNS zone in BunnyCDN.

## Endpoint

- **Method:** `POST`
- **Path:** `/dnszone`
- **Base URL:** `https://api.bunny.net`
- **Official documentation:** [Add DNS Zone](https://docs.bunny.net/reference/bunnynet-api-overview)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Domain` | body | `string` | yes | Domain name of the DNS zone. |
