# List BGP Active Prefixes with BigDataCloud

Retrieves active BGP prefixes from BigDataCloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/data/prefixes-list`
- **Base URL:** `https://api-bdc.net`
- **Official documentation:** [List BGP Active Prefixes](https://www.bigdatacloud.com/network-engineering/bgp-active-prefixes-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bogonsOnly` | query | `boolean` | no | Limit the response to bogon routes only. |
| `batchSize` | query | `number` | no | Requested batch size. Maximum value is 1000. |
| `offset` | query | `number` | no | Number of entries to skip. |
| `sort` | query | `string` | no | Sort by bgpPrefix, bgpPrefixNetworkAddress, bgpPrefixLastAddress, registryStatus, isBogon, isAnnounced, or carriers. |
| `order` | query | `string` | no | Sort order: asc or desc. |
| `asn` | query | `string` | no | Autonomous System Number as numeric or ASN format. |
| `localityLanguage` | query | `string` | no | Preferred language for localized country names. |
| `isv4` | query | `boolean` | no | When false, the response lists IPv6 prefixes. If omitted, IPv4 is assumed. |
