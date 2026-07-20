# List Tor Exit Nodes Geolocated with BigDataCloud

Retrieves geolocated Tor exit nodes from BigDataCloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/data/tor-exit-nodes-list`
- **Base URL:** `https://api-bdc.net`
- **Official documentation:** [List Tor Exit Nodes Geolocated](https://www.bigdatacloud.com/network-engineering/tor-exit-nodes-geolocated-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `batchSize` | query | `number` | no | Requested batch size. Maximum value is 1000. |
| `offset` | query | `number` | no | Number of entries to skip. |
| `sort` | query | `string` | no | Sort by ip, countryCode, countryName, or carriers. |
| `order` | query | `string` | no | Sort order: asc or desc. |
| `localityLanguage` | query | `string` | no | Preferred language for localized country names. |
