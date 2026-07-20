# List Networks by CIDR with BigDataCloud

Retrieves network details by CIDR from BigDataCloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/data/network-by-cidr`
- **Base URL:** `https://api-bdc.net`
- **Official documentation:** [List Networks by CIDR](https://www.bigdatacloud.com/network-engineering/networks-by-cidr-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cidr` | query | `string` | no | CIDR range in x.x.x.x/y format. |
| `depthLimit` | query | `number` | no | How many hierarchical levels down to include in the response. |
| `localityLanguage` | query | `string` | no | Preferred language for localized place and country names. |
| `subnetsBatchSize` | query | `number` | no | Number of subnetwork entries to retrieve. Default and hard limit are 20. |
| `subnetsOffset` | query | `number` | no | Number of subnetwork entries to skip. Default is 0. |
