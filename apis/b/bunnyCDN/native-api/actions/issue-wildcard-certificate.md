# Issue Wildcard Certificate with BunnyCDN

Issues a wildcard certificate for a BunnyCDN DNS zone.

## Endpoint

- **Method:** `POST`
- **Path:** `/dnszone/:zoneId/certificate/issue`
- **Base URL:** `https://api.bunny.net`
- **Official documentation:** [Issue Wildcard Certificate](https://docs.bunny.net/reference/bunnynet-api-overview)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `zoneId` | path | `string` | yes | The Bunny DNS zone ID. |
| `Domain` | body | `string` | yes | The wildcard domain that the certificate should be issued for. |
