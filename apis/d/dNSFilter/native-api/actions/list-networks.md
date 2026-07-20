# List Networks with DNSFilter

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/networks`
- **Base URL:** `https://api.dnsfilter.com`
- **Official documentation:** [List Networks](https://api.dnsfilter.com/docs#/paths/~1v1~1networks/get)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | no | Search among the network name, hostname, IP address, and related values. |
| `protected` | query | `boolean` | no | Filter networks with assigned policy. |
| `unprotected` | query | `boolean` | no | Filter networks without assigned policy. |
| `basic_info` | query | `boolean` | no | Return most basic Network Info only. Defaults to false. |
| `count_network_ips` | query | `boolean` | no | Return count of IP Addresses. Defaults to false. |
| `force_truncate_ips` | query | `boolean` | no | Return Network info without IP Addresses. Defaults to false. |
