# Bulk Lookup Domains with DNSFilter

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/domains/bulk_lookup`
- **Base URL:** `https://api.dnsfilter.com`
- **Official documentation:** [Bulk Lookup Domains](https://api.dnsfilter.com/docs#/paths/~1v1~1domains~1bulk_lookup/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fqdns` | query | `string` | no | Comma separated list of FQDNs to lookup |
