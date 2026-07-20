# Create Site with Ubiqod by Skiply

## Endpoint

- **Method:** `POST`
- **Path:** `/sites/`
- **Base URL:** `https://api.ubiqod.com`
- **Official documentation:** [Create Site](https://github.com/microsoft/PowerPlatformConnectors/tree/dev/certified-connectors/Ubiqod%20by%20Skiply%20(v2))

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `label` | body | `string` | yes | Site label. |
| `coordinates` | body | `object` | yes | Site coordinates object with latitude and longitude. |
| `distanceMargin` | body | `number` | no | Geofencing distance margin in meters. Ubiqod requires at least 50 when provided. |
| `externalReferences` | body | `object` | no | Optional external reference map for the site. |
