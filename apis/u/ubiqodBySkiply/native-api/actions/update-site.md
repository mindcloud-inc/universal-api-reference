# Update Site with Ubiqod by Skiply

## Endpoint

- **Method:** `PATCH`
- **Path:** `/sites/:siteId`
- **Base URL:** `https://api.ubiqod.com`
- **Official documentation:** [Update Site](https://github.com/microsoft/PowerPlatformConnectors/tree/dev/certified-connectors/Ubiqod%20by%20Skiply%20(v2))

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `siteId` | path | `string` | yes | Site ID. |
| `label` | body | `string` | no | Updated site label. |
| `coordinates` | body | `object` | no | Updated site coordinates object with latitude and longitude. |
| `distanceMargin` | body | `number` | no | Updated geofencing distance margin in meters. Ubiqod requires at least 50 when provided. |
| `externalReferences` | body | `object` | no | Updated external reference map for the site. |
